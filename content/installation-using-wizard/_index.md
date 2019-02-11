+++
title= "Installation using wizard"
date= 2018-03-09T11:06:25+05:30
description = ""
draft= false
weight = 2
+++

## Installation using wizard

### 1. APP Settings

![APP Settings](/images/installation_using_wizard/app_settings.png)

* `APP_NAME`

  This indicates the name of the application. You will see it at the top left bar.

* `APP_CURRENCY`

  It shows the currency that the system supports.

### 2. Database settings

![Database Settings](/images/installation_using_wizard/database_settings.png)

* `DB_CONNECTION`

  It indicates on which database server the application is required to get connected. It must be valued `MySQL`

* `DB_HOST`

  The database host to which the application will connect. Its value must be the host IP at which your database server is running. For example 127.0.0.1. If you are running the application using Docker, use database service name db as host.

* `DB_PORT`

  A port that database server listens. Generally, MySQL server listens at the port `3306`.

* `DB_DATABASE`

  Name of your database will be the value.

* `DB_USERNAME`

  The user of your MySQL server will be the value. By default, `mysql` has a user called `root`.

* `DB_PASSWORD`

  The value must be the password of your MySQL server to be connected. Mysql does not set any password by default.


### 3. Admin Settings(Initial User to setup the system)

![Admin Settings](/images/installation_using_wizard/admin_settings.png)

Below piece of configurations contains the information about the initial user who will install the system at the first stage.

* `Admin Name`

  Name of the admin.

* `Admin Email`

  E-mail of the admin who will install the system and seed initial data like an employee, store, etc.

* `Admin Password`

  Password for the above e-mail which is used while logging in to the system.


### Additional Settings

Following are the additional env fields which can be set directly in the `.env` file.

* `APP_TIMEZONE`

  This field specifies the timezone that the application will use for time-related operations. For example, `Asia/Kolkata`

* `APP_LANGUAGE`

  It serves the application in different languages. By default, we support application in two languages `en` and `da`.

* `QUEUE_DRIVER`

  It specifies how to send an e-mail to the user. Its value can be `sync` or `database`. For the `sync` value, the system will directly send e-mails rather than pushing it into a queue. For `Database`, system will generate jobs/queue and admin will have to run jobs explicitly.

* `Sentry`

  This is used to manage miscellaneous data. For example, a user can enable a field called "Send Anonymous Usage Data" to receive error logs for better user experience and improvement of application. To support this, the admin has to add sentry key in the .`env` file and enable the feature from settings.

* `ANALYTICS_PROVIDER`

  This sets up the analytics like google analytics. For example, `Google analytics`.

* `ANALYTICS_TRACKING_ID`

  It is related to analytics. Here we have to add tracking ID. For example, `UA-106769603-1`.
