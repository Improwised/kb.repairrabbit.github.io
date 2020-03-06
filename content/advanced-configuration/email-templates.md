+++
title= "Email Templates"
date= 2018-02-28T19:39:38+05:30
description = ""
draft= false
weight = 4
+++

* The system must have the following key settings in a `.env` file to send e-mails successfully from the system:

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

* These settings are also available on `settings` page of Admin. The keys in `.env` can also be changed from the settings panel.

## List Of Email Templates
* [Appointment Status Is No Show & Unconfirmed](/advanced-configuration/email-templates/#a-name-status-no-show-appointment-status-is-no-show-unconfirmed-a)
* [Appointment Confirmation Mail](/advanced-configuration/email-templates/#a-name-appointment-confirmation-appointment-conformation-mail-a)
* [Reminder E-Mail](/advanced-configuration/email-templates/#a-name-reminder-email-reminder-e-mail-a)
* [Appointment Notification To Store](/advanced-configuration/email-templates/#a-name-notification-to-store-appointment-notification-to-store-a)
* [New Ticket Creation](/advanced-configuration/email-templates/#a-name-new-ticket-new-ticket-creation-a)
* [Ticket Update](/advanced-configuration/email-templates/#a-name-ticket-update-ticket-update-a)
* [Password Reset](/advanced-configuration/email-templates/#a-name-password-reset-password-reset-a)
* [Ticket Notification To Store](/advanced-configuration/email-templates/#a-name-ticket-notification-to-store-ticket-notification-to-store-a)
* [New User Created](/advanced-configuration/email-templates/#a-name-ticket-notification-to-store-ticket-notification-to-store-a)
* [Ticket Updated With Policy Number](/advanced-configuration/email-templates/#a-name-ticket-update-with-policy-ticket-updated-with-police-number-a)
* [Retarget E-Mail Template](/advanced-configuration/email-templates/#a-name-retarget-email-template-retarget-e-mail-template-a)


### <a name="status_no_show">Appointment Status Is No Show & Unconfirmed</a>

An e-mail will be sent to the user when the appointment status is updated as `no_shows=1`.

### <a name="appointment_confirmation">Appointment Conformation Mail</a>

When the user creates an appointment, at that time a confirmation e-mail will be sent to the user.

### <a name="reminder_email">Reminder E-Mail</a>

An automatic reminder e-mail will be sent to the user for an appointment.

### <a name="notification_to_store">Appointment Notification To Store</a>

An e-mail notification will be sent to the store admin when new appointments created.

### <a name="new_ticket">New Ticket Creation</a>

An e-mail will be sent to the user when he/she creates a new ticket.

### <a name="ticket_update">Ticket Update</a>

An e-mail will be sent to the user when the status of the ticket is changed.

### <a name="password_reset">Password Reset</a>

An e-mail will be sent to the user when they request for password reset.

### <a name="ticket_notification_to_store">Ticket Notification To Store</a>

An e-mail will be sent to the store admin when a new ticket is created.

### <a name="new_user">New User Created</a>

An e-mail will be sent to the admin when a new user or an employee is registered in the system.

### <a name="ticket_update_with_policy">Ticket Updated With Policy Number</a>

An e-mail will be sent when the ticket policy number is updated.

### <a name="retarget_email_template">Retarget E-Mail Template</a>

An e-mail will be sent to the user when the appointment status gets updated as `retarget=1`.

## To Update Email Template

* To modify the e-mail template click "Edit", it will redirect the editor to change the name, subject, and status and content of a particular e-mail in that `{{variable_names}}` should be kept as it is.

* The `Active` status shows that the e-mail will be sent and the `Deactivate` status shows that the e-mail will not be sent from the system.

* The status can also be changed from the main listing of e-mail templates from admin side by clicking on `Active` or `Deactivate` button.
