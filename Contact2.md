---
layout: page
title: Contact (AWS Test)
---

Contact Us

<body>
  <div class="row">
    <div class="col-xs-8 col-xs-offset-2">
      <form class="form-horizontal" id="customer-contact-form" action="https://i1of1qng12.execute-api.us-east-1.amazonaws.com/dev/static-site-mailer" accept-charset="UTF-8" method="post" name="customer-contact-form">
        <div class="form-group contact_message_name">
          <label class="control-label" for="contact_message_name"><abbr title="Required">*</abbr> Name</label> <input class="form-control" placeholder="James Smith" type="text" name="name" id="contact_message_name" required="">
        </div>
        <div class="form-group contact_message_phone_or_email">
          <label class="control-label" for="contact_message_phone_or_email"><abbr title="Required">*</abbr> Phone or Email</label> <input class="form-control" placeholder="me@gmail.com" type="text" name="phone_or_email" id="contact_message_phone_or_email" required="">
        </div>
        <div class="form-group contact_message_text">
          <label class="control-label" for="contact_message_text"><abbr title="Required">*</abbr> Message</label> 
          <textarea rows="10" class="form-control" placeholder="Message text" name="text" id="contact_message_text" required=""></textarea>
        </div><br>
        <div class="alert alert-danger form-hidden" id="contact-form-failed-to-submit" role="alert">
          <strong>Failed to submit the form</strong> Please, try again.
        </div>
        <div class="alert alert-success form-hidden" id="contact-form-was-submitted" role="alert">
          <strong>Thank you!</strong> We will contact you.
        </div>
        <div class="form-actions">
          <button id="contact-form-loading-submit-button" name="button" class="btn btn-default btn-primary btn-lg form-hidden">Submitting...</button> <button id="contact-form-submit-button" name="button" type="submit" class="btn-default btn btn-primary btn-lg">Submit</button>
        </div>
      </form>
    </div>
  </div>
</body>