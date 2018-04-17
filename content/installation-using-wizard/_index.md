+++
title= "Installation using wizard"
date= 2018-03-09T11:06:25+05:30
description = ""
draft= false
weight = 2
+++

### 1. Environment settings

![Screen_Shot_2018-03-05_at_11.18.07_AM](https://gitlab.com/RepairRabbit/repairrabbit/uploads/b9e90e6422fe32cc88f76ed98db0d4a3/Screen_Shot_2018-03-05_at_11.18.07_AM.png)

* `APP_NAME`

  This denotes the name of the application. You will see it at the top left bar.

* `APP_ENV`

  It defines the running application environment. It can be Value as `local`, `development` and `production`.

* `APP_DEBUG`

  It specifies about debugs mode status as in or off. It can be valued as either `True` or `False`.

* `APP_LOG_LEVEL`

  It defines the active log level of the application. It can be Valued as any, `debug`, `info`, `notice`, `warning`, `error`, `critical`, `alert`, `emergency`.

* `APP_URL`

  The domain where the application is hosted. For example `http://demo.repairrabbit.com`

* `APP_LOGO`

  The application logo path. For example `http://repairrabbit.test/images/logo.png`

* `APP_CURRENCY`

  It shows the currency that system supports. Values should be any of the **HTML entity** from [here](https://www.toptal.com/designers/htmlarrows/currency/)

* `VAT`

  The applicable percentage value of VAT on all the price. By default system will consider `21`% of VAT included in Price.

### 2. Database settings

![Screen_Shot_2018-03-05_at_11.43.53_AM](https://gitlab.com/RepairRabbit/repairrabbit/uploads/63bdf40a3534ecf2780d9b59107d0048/Screen_Shot_2018-03-05_at_11.43.53_AM.png)

* `DB_CONNECTION`
  
  It denotes on which database server application required to get connected. It must be valued `mysql`

* `DB_HOST`

  The Database host to which application will connect. Its value must be host(ip) at which your database server is running. For example `127.0.0.1`. If you are running the application using Docker, use database service name `DB` as host.
  
* `DB_PORT`

  A Port that database server listens. Generally, MySQL server listens at the port `3306`.
  
* `DB_DATABASE`

  Name of your database will be the Value.
  
* `DB_USERNAME`

  The User of your MySQL server will the value. By default `mysql` has a user called `root`.
  
* `DB_PASSWORD`

  Value must be the password of your MySQL server to be connected.Mysql does not set any password by default.
  
* `DB_STRICT_MODE`

  It defines the mode to operate the database. The value should be either `True` or `False`.
  
### 3. Company Detail Settings for mail

![Screen_Shot_2018-03-05_at_11.44.14_AM](https://gitlab.com/RepairRabbit/repairrabbit/uploads/d2c76c9e5fffcf24f463719b298b7830/Screen_Shot_2018-03-05_at_11.44.14_AM.png)

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
  
### 4. Mail Settings

![Screen_Shot_2018-03-05_at_11.20.49_AM](https://gitlab.com/RepairRabbit/repairrabbit/uploads/013aa1134cffc77002b2f03020115c6f/Screen_Shot_2018-03-05_at_11.20.49_AM.png)

This piece of settings/configurations cotains information regarding mail settings. It has following configuration variables.

* `MAIL_DRIVER`

  It specifies which mail driver can be used while sending mails from the system. It's value can be any of the `mail`, `smtp`, `sendmail`, `mailgun`.

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

### 5. Admin Settings(Initial User to run)

![Screen_Shot_2018-03-05_at_11.47.23_AM](https://gitlab.com/RepairRabbit/repairrabbit/uploads/74765d15ed99b5f001c54676a61e5225/Screen_Shot_2018-03-05_at_11.47.23_AM.png)

Below piece of configurations contains the information about the initial user who will install the system at the first stage.

* `Admin Name `

  Name of the admin user.
  
* `Admin Email`

  Email of the admin user. Who will install the system and seed initial data like employee, stores, inventories etc.
  
* `Admin Password`

  Password for the above email. Which is used while login to the system.
  
  
### Additional Settings

Following are the additional env fields which can be set directly in `.env` file.

* `APP_TIMEZONE`

  This field specify timezone that application will use for time related operations. For example. `Asia/Kolkata`
  
* `APP_LANGUAGE`

  It serve the application in different languages. By default we support application in two languages `en`, `da`. You can add more languages if you need with the help of this instructions [here](./development/internationalization.md)
  
* `QUEUE_DRIVER`

  It specifies how to send an email to user. It value can be `sync` or `database`. for this `sync` value the system will directly send mails rather than pushing it into queue. For `Database` system will generate jobs/queue and admin will have to run jobs explicitely.
  
* `Sentry`

  This is used to manage miscellaneous data. For example user can enable a field called Send Anonymous usage data to receive error logs for better user experience and improvement of application. To support this, admin have to add sentry key in .env file. and enable feature from settings.
  
* `ANALYTICS_PROVIDER`

  This setup the analytics like google analytics. For example. `GoogleAnalytics`.
  
* `ANALYTICS_TRACKING_ID`

  It is related to anaylytics. Here we have to add tracking id.  For example. `UA-106769603-1`.
