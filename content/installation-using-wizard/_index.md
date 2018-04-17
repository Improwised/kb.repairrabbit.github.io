+++
title= "Installation using wizard"
date= 2018-03-09T11:06:25+05:30
description = ""
draft= false
weight = 2
+++

### 1. Environment settings

![Screen_Shot_2018-04-13_at_12.48.59_PM](https://gitlab.com/RepairRabbit/repairrabbit/uploads/c8ae45ed84f5f6284f0101992725fa54/Screen_Shot_2018-04-13_at_12.48.59_PM.png)

* `APP_NAME`

  This denotes the name of the application. You will see it at top left bar.


* `APP_CURRENCY`

  It shows the currency that system supports.

### 2. Database settings

![Screen_Shot_2018-04-13_at_12.49.30_PM](https://gitlab.com/RepairRabbit/repairrabbit/uploads/d9c6fe6e8c6ac7012dafb9ff6d337fba/Screen_Shot_2018-04-13_at_12.49.30_PM.png)

* `DB_CONNECTION`

  It denotes on which database server application required to get connected. It must be valued `mysql`

* `DB_HOST`

  The Database host to which application will connect. Its value must be host(ip) at which your database server is running. For example `127.0.0.1`. If you are running the application using docker, use database service name `db` as host.

* `DB_PORT`

  A Port that database server listen. Generally mysql server listen at the port `3306`.

* `DB_DATABASE`

  Name of your database will be the Value .

* `DB_USERNAME`

  The User of your mysql server will the value. By default `mysql` has user called `root`.

* `DB_PASSWORD`

  Value must be the password of your mysql server to be connected.Mysql does not set any password by default.


### 3. Admin Settings(Initial User to run)

![Screen_Shot_2018-04-13_at_12.50.22_PM](https://gitlab.com/RepairRabbit/repairrabbit/uploads/f64025750802732dfb274e73c0c25386/Screen_Shot_2018-04-13_at_12.50.22_PM.png)

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
