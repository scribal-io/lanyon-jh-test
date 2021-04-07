---
layout: page
title: Contact (Simplified)
---

<style> 
input[type=text], select {
  width: 100%;
  padding: 12px 20px;
  box-sizing: border-box;
  border: 2px solid #ccc;
  border-radius: 4px;
  background-color: #f8f8f8;
  font-size: 16px;
  resize: none;
  margin: 8px 0;
}

input[type=email], select {
  width: 100%;
  padding: 12px 20px;
  box-sizing: border-box;
  border: 2px solid #ccc;
  border-radius: 4px;
  background-color: #f8f8f8;
  font-size: 16px;
  resize: none;
  margin: 8px 0;
}

textarea {
  width: 100%;
  height: 150px;
  padding: 12px 20px;
  box-sizing: border-box;
  border: 2px solid #ccc;
  border-radius: 4px;
  background-color: #f8f8f8;
  font-size: 16px;
  resize: none;
}

input[type=submit] {
  width: 100%;
  background-color: #ac4142;
  color: white;
  padding: 14px 20px;
  margin: 8px 0;
  border: none;
  border-radius: 4px;
  font-size: 16px;
  cursor: pointer;
}

input[type=submit]:hover {
  background-color: #a9a9a9;
}

input[type=text]:hover {
  background-color: #f2f2f2;
}
.form-hidden {
      display: none;
}
/* The alert-danger message box */
.alert-danger {
  padding: 20px;
  color: white;
  background-color: #f44336; /* Red */
  font-family: Arial, Helvetica, sans-serif;
  margin-bottom: 15px;
}

/* The alert-success message box */
.alert-success {
  padding: 20px;
  color: white;
  background-color: #32A852; /* Green */
  font-family: Arial, Helvetica, sans-serif;
  margin-bottom: 15px;
}

/* The close button */
.closebtn {
  margin-left: 15px;
  color: white;
  font-weight: bold;
  float: right;
  font-size: 22px;
  line-height: 20px;
  cursor: pointer;
  transition: 0.3s;
}

/* When moving the mouse over the close button */
.closebtn:hover {
  color: black;
}
</style>

<form id="customer-contact-form" action="https://i1of1qng12.execute-api.us-east-1.amazonaws.com/dev/static-site-mailer" accept-charset="UTF-8" method="post" name="customer-contact-form">
  <input type="text" name="name" id="contact_message_name" placeholder="enter your name" required><br/>
  <input type="email" name="email" id="contact_message_phone_or_email" placeholder="enter your email" required><br/>
  <textarea name="message" id="contact_message_text" placeholder="tell us what's on your mind" required></textarea><br/>
  <input type="submit" value="Submit">
  <div class="alert alert-danger form-hidden" type="text" id="contact-form-failed-to-submit" role="alert"> <strong>Failed to submit the form. Please, try again. </strong>
  </div>
 <div class="alert-success form-hidden" type="text" id="contact-form-was-submitted" role="alert">
  <span class="closebtn" onclick="this.parentElement.style.display='none';">&times;</span> 
 <strong>Thank you! We have received your message. </strong>
</div>
</form>


<!--
<div class="alert alert-success form-hidden" type="text" id="contact-form-was-submitted" role="alert">
#4CAF50
<button>Submit</button>

div {
  border-radius: 5px;
  background-color: #f2f2f2;
  padding: 20px;
}

<div style="position: absolute; left: -5000px;">
  <input type="checkbox" name="furry_almond_honeycomb_safe" value="1" tabindex="-1" autocomplete="no">
</div>
cols="30" rows="10"
<body>
    <div>
      <form id="customer-contact-form" action="https://i1of1qng12.execute-api.us-east-1.amazonaws.com/dev/static-site-mailer" accept-charset="UTF-8" method="post" name="customer-contact-form">
        <div class="form-group contact_message_name">
          <label class="control-label" for="contact_message_name"><abbr title="Required">*</abbr> Name</label> <input class="form-control" placeholder="James Smith" type="text" name="name" id="contact_message_name" required="required">
        </div>
        <div class="form-group contact_message_phone_or_email">
          <label class="control-label" for="contact_message_phone_or_email"><abbr title="Required">*</abbr> Phone or Email</label> <input class="form-control" placeholder="me@gmail.com" type="text" name="phone_or_email" id="contact_message_phone_or_email" required="">
        </div>
        <div class="form-group contact_message_text">
          <label class="control-label" for="contact_message_text"><abbr title="Required">*</abbr> Message</label> 
          <textarea rows="10" class="form-control" placeholder="Message text" type="textarea" id="contact_message_text" required=""></textarea>
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
</body>
-->