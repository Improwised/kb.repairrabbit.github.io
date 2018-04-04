+++
title= "Installation"
date= 2018-01-18T19:42:39+05:30
description = ""
draft= false
type="page"
weight = 1
+++


### Cloud setup:

#### Prerequisites:

* docker/docker-compose
* git

Project should be added on your server and make sure that you are in the project root.

Run the below command from the project root.

```
docker-compose up
```

It will create 3 containers for nginx, app and database respectively. 

As we mount the storage to the container. Give read/write permission to storage for user docker.

```
chmod -R 777 storage/app/public/
```

Once the containers are created Successfully , follow this command to get into the `app` container. `docker exec -it <container> bash`.

* Now generate an application key

```
php artisan key:generate

```

* Link the storage

```
php artisan storage:link
```

To know detail description of each configuration variables [click](/wizard-installation/).

### Shared Hosting Setup

Lets assume you have extracted the zip package and you served `index.php` from public folder.

* Go to installation route

  ```
  {APP_URL}/install
  ```

* Provide `Environment`, `Database`, `Company`, `Mail` and one `super admin` user information to kickstart the application.

* Wizard will set the configurations required for this ERP.

* To know the details of each configuration variables [click](/wizard-installation/)


#### Miscellaneous

If you fail to generate PDF on server, create a `fonts` folder into the storage folder.
