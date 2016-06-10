# Secure Your Forms With Form Keys

Read:  
https://code.tutsplus.com/tutorials/secure-your-forms-with-form-keys--net-4753

Demo:  
http://jillella.com/SecureYourFormsWithFormKeys/

## Topic Highlights

#### Secure Your Forms With Form Keys

Security is a hot topic. Ensuring that your websites are secure is extremely important for any web application. One of the most important things we must secure are forms. Today, we are going to review a method to prevent XSS (Cross-site scripting) and Cross-site request forgery on forms.

#### Why?
POST data can be sent from one website to another. Why is this bad? A simple scenario...

> A user, logged into your website, visits another website during his session. This website will be able to send POST data to your website -- for example, with AJAX. Because the user is logged in on your site, the other website will also be able to send post data to secured forms that are only accessible after a login.

#### How Do We Fix This?
With form keys! We'll add a special hash (a form key) to every form to make sure that the data will only be processed when it has been sent from your website. After a form submit, our script will validate the submitted form key against the form key we've set in a session.

#### What We Must Do:
  1. Add a form key to every form.
  2. Store the form key in a session.
  3. Validate the form key after a form submit.

#### Conclusion:
Adding this code to every important form on your website will increase your form's security dramatically. It even stops refreshing issues. Because the form key is only valid for one request, a double post is not possible.
