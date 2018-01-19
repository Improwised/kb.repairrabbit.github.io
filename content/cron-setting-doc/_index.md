+++
title= "Cron Setting Doc"
date= 2018-01-18T19:23:21+05:30
description = ""
weight = 99
draft= false
alwaysopen = true
+++

The documentation for Repair Rabbit api is provided here in this file

### Documetation for setting up cron and email queue

* Check .env file for `QUEUE_DRIVER`, it must be `database`.
* Then if you want to send email from system then please check the email status from admin email templates.
* If the email having `deactive` status then it can't make the entery in `jobs` table of your database so be sure it is `active`.
* Then check your mail configuration in environment file it must require the following things:

```
MAIL_DRIVER=smtp
MAIL_HOST=smtp.sendgrid.net
MAIL_PORT=587
MAIL_USERNAME=abc@gmail.com
MAIL_PASSWORD=abc
MAIL_ENCRYPTION=null
MAIL_FROM_ADDRESS=abc1@gmail.com
MAIL_FROM_NAME=abc1
```

* After that if you visit any link in that mail system is there for example register new user in user side application then you got the new entry in jobs table in your database.
* To execute the all jobs entey please follow the following things:

### To run the schedule in local system

```
php artisan schedule:run
```

* Because of some problem if jobs will not be executed successfully then it tries to execute 3 times after that it will make the entry in `failed_jobs` table of your database


### To retrive the failed job back to execute again run the following:

```
php artisan queue:retry all
```

* This command will recover all enteries from `failed_jobs` to `jobs` table of your database.

### deploy on server

You have to find php exectuable path in the server. For an instance, it can be setup inside cron as :

```
 * * * * * cd /home/path to project -folder && /usr/local/bin/php artisan schedule:run >> /home/path-where-you-want-output/cron-output.txt 2>&1 2>&1
```


