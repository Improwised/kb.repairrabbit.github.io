+++
title= "Installation"
date= 2018-01-18T19:42:39+05:30
description = ""
draft= false
type="page"
weight = 1
+++

### Setup On Cloud
Install project

```
git clone git@gitlab.com:RepairRabbit/repairrabbit.git
```

Change Directory

```
cd repairrabbit
```

Install all dependencies

```
composer install
```

Create a .env file

```
Create a .env file in root of the prject as per `.env.example` supplied. (you can setup .env file through wizard also)
```

Generate application key

```
php artisan key:generate
```

Link the storage

```
php artisan storage:link
```

Create database in mysql

```
create database `databaseName`
```

Database migration

```
php artisan migrate

```

Serve Application

```
php artisan serve
```

Alternatively you can serve using [valet](https://laravel.com/docs/5.4/valet#installation)

Link url to valet for that go to that directory and run following command

```
valet link
```

After link that valet to get the url

```
valet links
```

From links select your project url and Open in browser
For example,

```
http://phoneworld.dev
```

#### Using Docker

Run below command in root of your project.

```
docker-compose up
```

Above command will create 3 containers for nginx, app and database respectively. For `.env` settings [click here](/wizard-env/).

### Setup On Shared Hosting

Here we assume you have whole application's repository including `vendor` and database setup already done and you served the application already.

* Go to installation route

  ```
  {APP_URL}/install
  ```

* Provide `Environment`, `Database`, `Company`, `Mail` and one `super admin` user information to kickstart the application.

* Wizard will generate `.env` file and set the configurations required for this ERP.
* To know detail description of each `.env` variables [click here](/wizard-env/)

