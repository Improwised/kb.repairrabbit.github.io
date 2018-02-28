+++
title= "Email Templates"
date= 2018-02-28T19:39:38+05:30
description = ""
draft= false
weight = 4
+++

* The system must have following key settings in `.env` file to send mail successfully from system:

```
COMPANY_EMAIL_SUPPORT=
COMPANY_EMAIL_INFO=
COMPANY_POLICY_SERVICE_MAIL=

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

(in case of mailgun)
MAILGUN_DOMAIN=
MAILGUN_SECRET=
```

* These settings also available in `settings` page of admin. These keys in `.env` se can also be changed from settings panel.

## List Of Email Templates

* [Appointment Status Is No Show & Unconfirmed](#status_no_show)
* [Appointment confirmation Mail](#appointment_confirmation)
* [Reminder E-Mail](#reminder_email)
* [Appointment Notification To Store](#notification_to_store)
* [New Ticket Creation](#new_ticket)
* [Ticket Update](#ticket_update)
* [Password Reset](#password_reset)
* [Ticket Notification To Store](#ticket_notification_to_store)
* [New User Created](#new_user)
* [Ticket Updated With Police Number](#ticket_update_with_policy)
* [Retarget E-Mail Template](#retarget_email_template)


### <a name="status_no_show">Appointment status is no show & unconfirmed</a>

Email will be sent to user, When the appointment status updated as `no_shows=1`.

### <a name="appointment_confirmation">Appointment conformation mail</a>

When user creates an appointment at that time an confirmation mail will be sent to user.

### <a name="reminder_email">Reminder E-Mail</a>

An automatic reminder email will be sent to user for an appointment.

### <a name="notification_to_store">Appointment Notification to Store</a>

An email notification will be sent to store admin when new appoinments created.

### <a name="new_ticket">New Ticket Creation</a>

An email will be sent to user when he/she creates new ticket.

### <a name="ticket_update">Ticket Update</a>

An email will be sent to user when the status of ticket changed.

### <a name="password_reset">Password Reset</a>

An email will be sent to user when it request for password reset.

### <a name="ticket_notification_to_store">Ticket Notification to Store</a>

An email will be sent to store admin when new ticket created.

### <a name="new_user">New User Created</a>

An email will be sent to admin when new user or employee register in the system.

### <a name="ticket_update_with_policy">Ticket Updated With Police Number</a>

An email will be sent when ticket policy number updated.

### <a name="retarget_email_template">Retarget E-Mail Template</a>

An email will be sent to user when the appointment status will be updated as `retarget=1`.

## To Update Email Template

* To modify the email templete from `Edit` button, It will redirecting the ckeditor to change the name, subject, status and content of a perticular mail in that `{{variable_names}}` should be keep as it is to replace it with actual value in mail.

* The `Active` status shows that the mail will be sent and the `Deactive` status shows the mail will not be sent from system.

* The status can also be changed from main listing of email-templates at admin side by clicking on `Active` or `Deactive` button.
