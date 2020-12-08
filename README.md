<<<<<<< Updated upstream
# Test
=======
# Scribal Website/Blog

The Scribal website is based on the Lanyon Jekyll theme and hosted at Github Pages (GHP). Jekyll is an open-source Ruby-based static website generator. It is well integrated with Github and is probably the easiest way to get a DIY website up and running quickly.

One tricky aspect of GHP is deploying a custom Jekyll theme if you want to use somethng other than themes directly integrated by Github. We opted for Lanyon because of its clean design, because it integrates a side-drawer which enables us to display basic "About" and "Contact" info for our company, and because Lanyon itself has options which let the user modify the look and feel.

In addition to replicating the [Lanyon](Lanyon) readme (below), this file documents  modifications specific to deploying on Git and to our use of Lanyon and GHP here at Scribal.

## Deployment on Github Pages

The way that Github Pages works is that Github recognizes any directory that has the Jekyll file structure and with a one-click configuration in settings builds and deploys to a public URL. This works easily if you use the default theme (Minima) or one of a small handful of addtional themes offered in a repository's settings. However, if you want to use any other custom theme (and there are dozens available) deploying it properly can be difficult, despite the efforts of the theme designers. 

Lanyon contains a fair amount of CSS so getting the settings for relative/absolute links is important. It's not enough to run Lanyon on a locally-hosted Jekyll instance because the [Github production version of Jekyll and related ruby gems](https://pages.github.com/versions/) may be different than what you are running locally. It's worth checking the linked page if you run into difficulties.

The most important thing for getting Lanyon to run properly on GHP are the links in the .'config_yml' file in the repo's home directory. There is an important distinction to make between sites that use a custom URL and those which use the default GHP URLs:
- if using a custom URL copy it into the URL slot in "Setup" and leave the 'baseurl' slot blank. You also have to create a CNAME file in the home directory which contains text pointing to your CNAME info. [Full documentation on how to configure this can be found here](https://docs.github.com/en/free-pro-team@latest/github/working-with-github-pages/managing-a-custom-domain-for-your-github-pages-site).
- if you are using the GHP default URL, the 'url' slot should be left blank and there shouldn't be any 'CNAME' file in the home directory. Instead, the 'baseurl' slot should be filled in with the name of the repo in Unix directory style (for this site it is - '/lanyon-jh-test/'). It took a lot of trial and error to get this to run correctly.

Here are some helpful documentation resources for deploying a Lanyon site:
- [Building your own Personal Website in Jekyll](https://chrisschuld.com/2019/02/building-your-own-website-in-jekyll/)
- [How to set up lanyon-plus jekyll theme](https://davidbarber.github.io/readme/)


## Blogging Workflow

When Github pages detects changes in your repo, those changes are automatically deployed to the web. When multiple users have commit permission to the repo, there is always the possiblity of conflicting changes. Some rules of thumb to minimize the chances that this will cause problems either with a user's local copy of the repo or (less likely, but more disastrously) with the deployed site:
- Make sure to pull an up-to-date version of the repo before starting to make changes. The Git command that makes this easiest is 'git pull -- rebase' - for more complete explanation of how to use git to sync changes and updates [this blog post is helpful](https://supercollider.github.io/development/git-cheat-sheet).
- If we reach a point where there are multiple contributors to the site, one way to manage it is to designate a 'webmaster' with control over the repo and make everyone else fork the repo and have them submit pull requests in order for a post to appear on the production site.
>>>>>>> Stashed changes

# Lanyon

Lanyon is an unassuming [Jekyll](http://jekyllrb.com) theme that places content first by tucking away navigation in a hidden drawer. It's based on [Poole](http://getpoole.com), the Jekyll butler.

![Lanyon](https://f.cloud.github.com/assets/98681/1825266/be03f014-71b0-11e3-9539-876e61530e24.png)
![Lanyon with open sidebar](https://f.cloud.github.com/assets/98681/1825267/be04a914-71b0-11e3-966f-8afe9894c729.png)


## Contents

- [Usage](#usage)
- [Options](#options)
  - [Sidebar menu](#sidebar-menu)
  - [Themes](#themes)
  - [Reverse layout](#reverse-layout)
- [Development](#development)
- [Author](#author)
- [License](#license)


## Usage

Lanyon is a theme built on top of [Poole](https://github.com/poole/poole), which provides a fully furnished Jekyll setup—just download and start the Jekyll server. See [the Poole usage guidelines](https://github.com/poole/poole#usage) for how to install and use Jekyll.


## Options

Lanyon includes some customizable options, typically applied via classes on the `<body>` element.


### Sidebar menu

Create a list of nav links in the sidebar by assigning each Jekyll page the correct layout in the page's [front-matter](http://jekyllrb.com/docs/frontmatter/).

```
---
layout: page
title: About
---
```

**Why require a specific layout?** Jekyll will return *all* pages, including the `atom.xml`, and with an alphabetical sort order. To ensure the first link is *Home*, we exclude the `index.html` page from this list by specifying the `page` layout.


### Themes

Lanyon ships with eight optional themes based on the [base16 color scheme](https://github.com/chriskempson/base16). Apply a theme to change the color scheme (mostly applies to sidebar and links).

![Lanyon with red theme](https://f.cloud.github.com/assets/98681/1825270/be065110-71b0-11e3-9ed8-9b8de753a4af.png)
![Lanyon with red theme and open sidebar](https://f.cloud.github.com/assets/98681/1825269/be05ec20-71b0-11e3-91ea-a9138ef07186.png)

There are eight themes available at this time.

![Available theme classes](https://f.cloud.github.com/assets/98681/1817044/e5b0ec06-6f68-11e3-83d7-acd1942797a1.png)

To use a theme, add any one of the available theme classes to the `<body>` element in the `default.html` layout, like so:

```html
<body class="theme-base-08">
  ...
</body>
```

To create your own theme, look to the Themes section of [included CSS file](https://github.com/poole/lanyon/blob/master/public/css/lanyon.css). Copy any existing theme (they're only a few lines of CSS), rename it, and change the provided colors.


### Reverse layout

![Lanyon with reverse layout](https://f.cloud.github.com/assets/98681/1825265/be03f2e4-71b0-11e3-89f1-360705524495.png)
![Lanyon with reverse layout and open sidebar](https://f.cloud.github.com/assets/98681/1825268/be056174-71b0-11e3-88c8-5055bca4307f.png)

Reverse the page orientation with a single class.

```html
<body class="layout-reverse">
  ...
</body>
```


### Sidebar overlay instead of push

Make the sidebar overlap the viewport content with a single class:

```html
<body class="sidebar-overlay">
  ...
</body>
```

This will keep the content stationary and slide in the sidebar over the side content. It also adds a `box-shadow` based outline to the toggle for contrast against backgrounds, as well as a `box-shadow` on the sidebar for depth.

It's also available for a reversed layout when you add both classes:

```html
<body class="layout-reverse sidebar-overlay">
  ...
</body>
```

### Sidebar open on page load

Show an open sidebar on page load by modifying the `<input>` tag within the `sidebar.html` layout to add the `checked` boolean attribute:

```html
<input type="checkbox" class="sidebar-checkbox" id="sidebar-checkbox" checked>
```

Using Liquid you can also conditionally show the sidebar open on a per-page basis. For example, here's how you could have it open on the homepage only:

```html
<input type="checkbox" class="sidebar-checkbox" id="sidebar-checkbox" {% if page.title =="Home" %}checked{% endif %}>
```

## Development

Lanyon has two branches, but only one is used for active development.

- `master` for development.  **All pull requests should be to submitted against `master`.**
- `gh-pages` for our hosted site, which includes our analytics tracking code. **Please avoid using this branch.**


## Author

**Mark Otto**
- <https://github.com/mdo>
- <https://twitter.com/mdo>


## License

Open sourced under the [MIT license](LICENSE.md).

<3
