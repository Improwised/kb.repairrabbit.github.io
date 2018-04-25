+++
title= "Installation"
date= 2018-01-18T19:42:39+05:30
description = ""
draft= false
type="page"
weight = 1
+++

### Setup On Cloud

#### Prerequisites:

* docker/docker-compose >= 18.03.0/1.18.0

You must have added the project on your server/machine and you are in root of your project.

Change values of exported variables in `setup.sh` file in case if you want. Most of the cases the default values will work.

```
export NGINX_PORT=80
export APP_PORT=9000
export DB_PORT=33061

export MYSQL_ROOT_PASSWORD=secret
export MYSQL_DATABASE=repairrabbit
export MYSQL_USER=root
```

Run `setup.sh` file to start installation

```
sh setup.sh
```
or

```
sh setup.sh up
```
Now, Wait for the installation to complete

once the installation completes, you can access the application at `{YOUR IP}:{NGINX_PORT}`.

For example `192.168.1.26:80`, `127.0.0.1:80`.

To know detail description of each configuration variables [click here](/installation-using-wizard/).

### Shared Hosting Setup

Lets assume you have extracted the zip package and you served `index.php` from public folder.

* Go to installation route

  ```
  {APP_URL}/install
  ```

* Provide `Environment`, `Database`, `Company`, `Mail` and one `super admin` user information to kickstart the application.

* Wizard will set the configurations required for this ERP.

* To know the details of each configuration variables [click here](/installation-using-wizard/)


#### Miscellaneous

If you fail to generate PDF on server, create a `fonts` folder into the storage folder.
