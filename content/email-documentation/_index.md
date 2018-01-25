+++
title= "RepairRabbit Email Documentation"
date= 2018-01-18T19:38:41+05:30
description = ""
draft= true
alwaysopen = true
+++

A documentation for mails which gives idea to user, what mails we send from the our system, what is the purpose of each mails, when they get send, how to modify email template, things to consider before changing mail template, how to disable/enable mails etc.

* The system must having the following key settings from `.env` file to send mail successfully from system:

```
APP_LOGO=

COMPANY_NAME=
COMPANY_PHONE=
COMPANY_EMAIL_SUPPORT=
COMPANY_EMAIL_INFO=
COMPANY_WEBSITE=
COMPANY_POLICY_SERVICE_MAIL=

QUEUE_DRIVER=

MAIL_DRIVER=
MAIL_HOST=
MAIL_PORT=
MAIL_USERNAME=
MAIL_PASSWORD=
MAIL_ENCRYPTION=
MAIL_FROM_ADDRESS=
MAIL_FROM_NAME=
MAIL_REPLY_ADDRESS=
MAIL_REPLY_NAME=

MAILGUN_DOMAIN=
MAILGUN_SECRET=
```

* These settings also available in `settings` page of admin, by using that we also changed this all environment settings.

## To Update Email Template
* To modify the email templete from `Edit` button, It will redirecting the ckeditor to change the name, subject, status and content of a perticular mail in that `{{variable_names}}` should be keep as it is to replace it with actual value in mail.
* The `Active` status shows that the mail will be sent and the `Deactive` status shows the mail will not be sent from system.
* The status can also be changed from main listing of email-templates at admin side by clicking on `Active` or `Deactive` button.

## Email template list

We are providing the following sample email templates with the possible ways when this mail will be sent:

**Appointment status is no show & unconfirmed**

```
When the appointment status will be updated as `no_shows=1` from admin to user
```

**Appointment conformation mail**

```
New appointment creation from admin and user
```

**Reminder E-Mail**

```
For automatic reminder to repair appointment from admin to user
```

**Appointment Notification to Store**

```
For automatic notification when the new appointment will be created for that perticualr store
```

**New Ticket Creation**

```
For user about new ticket being created
```

**Ticket Update**

```
For user about ticket status updated from admin
```

**Password reset**

```
For sending the new password from admin to user(Reset Password at admin and user, Change Password of customer and employee at admin)
```

**New User Created**

```
New user creation at user
New customer creation at admin
New employee creation in store at admin
```

**Ticket updated with Police number**

```
When the ticket updated with it's police number and it will notify to company's policy service
```

**Retarget E-Mail template**

```
When the appointment status will be updated as `retarget=1` from admin to user
```

