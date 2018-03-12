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
* git

You must have project added on your server and you are in root of your project.

Run below command from root of your project.

```
docker-compose up
```

Above command will create 3 containers for nginx, app and database respectively. 

As we mount the storage to container. Give read/write permission to storage for user docker.

```
chmod -R 777 storage/app/public/
```

After Successfull creation of containers. SSH/Bash into app container using `docker exec -it <container> bash`.

* Generate application key

```
php artisan key:generate

```

* Link the storage

```
php artisan storage:link
```

To know detail description of each configuration variables [click here](/wizard-installation/).

### Setup On Shared Hosting

Here we assume you have extracted the zip package and you served `index.php` from public folder.

* Now, Go to installation route

  ```
  {APP_URL}/install
  ```

* Provide `Environment`, `Database`, `Company`, `Mail` and one `super admin` user information to kickstart the application.

* Wizard will set the configurations required for this ERP.

* To know detail description of each configuration variables [click here](/wizard-installation/)


#### Miscellaneous

If you are unable to generate PDF on server, create a folder fonts inside storage folder.
