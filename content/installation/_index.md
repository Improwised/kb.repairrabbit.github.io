+++
title= "Installation"
date= 2018-01-18T19:42:39+05:30
description = ""
draft= false
type="page"
weight = 1
+++

### How to Setup On Cloud

**Setup repairrabiit on cloud using docker  :**

For dockerize repairrabbit follow this [document](https://github.com/Improwised/dockerize-repairrabbit).
### Shared Hosting Setup

Let's assume you have extracted the zip package and you served `index.php` from the public folder.

* Go to installation route

  ```
  {APP_URL}/install
  ```

* Provide `Environment`, `Database`, `Company`, `Mail` and one `Super admin` user information to kickstart the application.

* Wizard will set the configurations required for this ERP.

* To know the details of each configuration variable [click here](/installation-using-wizard/)


#### Note

If you fail to generate PDF on a server, create a `fonts` folder in the storage folder.
