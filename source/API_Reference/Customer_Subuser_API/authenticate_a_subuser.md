---
layout: page
weight: 0
title: Authenticate a Subuser
navigation:
   show: true
---

Authenticate a subuser on your website before displaying their account information so that you can have users manage their SendGrid account on your website.

<table class="table table-bordered table-striped">
   <tbody>
      <tr>
         <th>Parameter</th>
         <th>Required</th>
         <th>Requirements</th>
      </tr>
      <tr>
         <td>user</td>
         <td>Yes</td>
         <td>Subuser that is registered under your account.</td>
      </tr>
      <tr>
         <td>password</td>
         <td>Yes</td>
         <td>Password the subuser submitted.</td>
      </tr>
   </tbody>
</table>

{% apiexample auth POST https://api.sendgrid.com/apiv2/customer.auth api_user=your_sendgrid_username&api_key=your_sendgrid_password&user=example@example.com&password=theirsubmittedpassword %}
  {% response json %}
{
  "message": "success"
}
  {% endresponse %}
  {% response xml %}
<?xml version="1.0" encoding="ISO-8859-1"?>

<result>
   <message>success</message>
</result>

  {% endresponse %}
{% endapiexample %}