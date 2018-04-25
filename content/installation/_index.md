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

* docker/docker-compose

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

Give executable permission to `setup.sh` file.

```
chmod +x setup.sh
```

Run `setup.sh` executable.

```
sh setup.sh

```
Or to Rebuild application:

```
sh setup.sh up

```

Above command will create 3 containers for nginx, app and database respectively.

As we mount the storage to container. Give read/write permission to storage for user docker.

```
chmod -R 777 storage/app/public/
```
Link the storage

```
php artisan storage:link
```
Now, You can access the application at `{YOUR IP}:{NGINX_PORT}`.

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

* To know the details of each configuration variables [click](/installation-using-wizard/)


#### Miscellaneous

If you fail to generate PDF on a server, create a `fonts` folder into the storage folder.
