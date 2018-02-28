+++
title= "Wizard Env"
date= 2018-02-28T17:24:37+05:30
description = ""
draft= false
+++

**1. Environment settings**

* `APP_NAME`

  This field denotes the name of the application. You will see it at top left bar.

* `APP_ENV`

  It defines the environment in which application is running. Value can be `local`, `development` and `production`.

* `APP_DEBUG`

  It specifies whether debug mode is on or off. It's value can be either `True` or `False`.

* `APP_LOG_LEVEL`

  It is used to define which log level, the application is using. Value can be  any of `debug`, `info`, `notice`, `warning`, `error`, `critical`, `alert`, `emergency`.

* `APP_URL`

  The domain where the application is hosted. For example `http://demo.repairrabbit.com`

* `APP_LOGO`

  The path at which the logo of the application is available. For example `http://repairrabbit.test/images/logo.png`

* `APP_CURRENCY`

  It shows the currency which would be used in entire system. Values should be any of the **html entity** from [here](https://www.toptal.com/designers/htmlarrows/currency/)

* `VAT`

  The percentage value of VAT, That would be applied to all the price. By default it would consider `21`% of VAT included in Price.


**2. Database settings**

* `DB_CONNECTION`
  
  database server to which to connect. It value must be `mysql`

* `DB_HOST`

  The database host to connect application. Its value must be host(ip) at which your database server is running. For example `127.0.0.1`
  
* `DB_PORT`

  Port at which your database server listen. Generally mysql server listen at port `3306`.
  
* `DB_DATABASE`

  Value must be the name of your database.
  
* `DB_USERNAME`

  Value must be the user of your mysql server. By default `mysql` has user called `root`.
  
* `DB_PASSWORD`

  Value must be the password of your mysql server to be connected. By default mysql does not set any password.
  
* `DB_STRICT_MODE`

  It defines the mode in which to operate database. It should contains value either `True` or `False`.
  

**3. Company Detail Settings for mail**

* `COMPANY_NAME`

  It shows the name of the company. For example `RepairRabbit`.
  
* `COMPANY_PHONE`

  It consist the phone number of the company.
  
* `COMPANY_EMAIL_SUPPORT`

  Email address for support.
  
* `COMPANY_EMAIL_INFO`

  Email address for general information.
  
* `COMPANY_WEBSITE`

  Url of the company's website. For example `http://repairrabbit.co`
  
* `COMPANY_POLICY_SERVICE_MAIL`

  This email would be used to communicate regarding company's policy services.
  

**4. Mail Settings**

This piece of settings/configurations cotains information regarding mail settings. It has following configuration variables.

* `MAIL_DRIVER`

  It specifies which mail driver would be used while sending mails from the system. It's value can be any of the `mail`, `smtp`, `sendmail`, `mailgun`.

* `MAIL_FROM_NAME`

  The `MAIL_FROM_NAME` would be used along with mail.
  
* `MAIL_USERNAME`

  It specifies the username used by mail driver. It used for authentication.
  
* `MAIL_PASSWORD`

  It consist the password for the particular mail service.
  
* `MAIL_HOST`

  It is similar to database host field. But here it consist the host for mail server.
  
* `MAIL_PORT`

  The port at which the mail server listen the incomming request.
  
*  `MAIL_ENCRYPTION`

  It shows which enctyption to used while sending mail. It can be any of the following. `tls`, `ssl`, `none`.
  
* `MAIL_REPLY_NAME`

  This value will be shown to user when they reply to mail.
  
* `MAIL_REPLY_ADDRESS`
  
  User will reply to this mail address when they click on reply. the reply address would be set by this value. 

* `MAILGUN_DOMAIN`

  This field is specific to mailgun driver. It contains the value of domain required for mailgun.
  
* `MAILGUN_SECRET`
  
  This field is also specific to mailgun. It contains the secret key provided by mailgun for authentication.

* `Test Email`

  Mail address to test connection.

**5. Admin Settings(Initial User to run)**

Below piece of configurations contains the information about the initial user who will gonna setup the system first.

* `Admin Name `

  Name of the initial user.
  
* `Admin Email`

  Email of the initial admin user. Who will gonna setup the system and seed initial data like employee, stores, inventories etc.
  
* `Admin Password`

  Password for the above email. Which is used while login to the system.
