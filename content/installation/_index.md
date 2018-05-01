+++
title= "Installation"
date= 2018-01-18T19:42:39+05:30
description = ""
draft= true
type="page"
weight = 1
+++

### How to Setup On Cloud

#### Prerequisites:

* docker/docker-compose >= 18.03.0/1.18.0

You must have added the project to your server/machine and you are in the root of your project.

In Most of the cases the default values will work and also you can Change values of exported variables in `setup.sh` file.

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

Now, Wait for the installation to complete

once the installation completes, you can access the application at `{YOUR IP}:{NGINX_PORT}`.

For example `192.168.1.26:80`, `127.0.0.1:80`.

To know detail description of each configuration variables [click here](/installation-using-wizard/).

### Shared Hosting Setup

Let's assume you have extracted the zip package and you served `index.php` from the public folder.

* Go to installation route

  ```
  {APP_URL}/install
  ```

* Provide `Environment`, `Database`, `Company`, `Mail` and one `super admin` user information to kickstart the application.

* Wizard will set the configurations required for this ERP.

* To know the details of each configuration variables [click here](/installation-using-wizard/)


#### Note

If you fail to generate PDF on a server, create a `fonts` folder into the storage folder.
