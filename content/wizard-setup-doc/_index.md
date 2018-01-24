+++
title= "Product Installation Guide for Wizard"
date= 2018-01-18T19:42:39+05:30
description = ""
draft= true
type="page"
+++

The documentation for Repairrabbit product to use it :

## Prerequisites

* [Laravel 5.4](http://laravel.com/)
* [MySQL] (https://www.mysql.com/downloads/)

## Instructions

* Link the directory into valet
* Open the valet linked url in browser
* Go to `{domain}/install` route
* After that click on `Check Requirements`, it shows server requirements page
* After that click on `Check Permissions`, it shows permissions page for folders
* After that click on `Configure Environment`, it shows form to set up `.env` file
    It contains five setps to generate `.env`:

**1. Environment settings**
```
App Name
App Environment
App Debug
App Log Level
App Url
App Logo Url
App Currency
```

**2. Database settings**
```
Database Connection
Database Host
Database Port
Database Name
Database Username
Database Password
(After adding this detail please check `Test Db Connection` before moving ahead)
```

**3. Company Detail Settings for mail**
```
Company Name
Company PhoneNo.
Company Support Email Address
Company Information Email Address
Company Website
Company Policy Service Email
```

**4. Mail Settings**
```
Mail Driver
Mail From Name
Mail From Address
Mail Username
Mail Host
Mail Port
Mail Password
Mail Encryption
Mail Reply Name
Mail Reply Address
Test Email(To test the mail connection)
(After adding this detail please check `Test Mail Connection` before moving ahead)
```

**5. Admin Settings(Initial User to run)**
```
Admin name
Admin email
Admin password
(This detail will be seeded as initial user in database.)
```

* After submitting all detail for environment setup, it will showing the `Installation Finished` screen in that click on `click here to exit` button.
* The migration also run from this process and one user also added in `users` table and `roles`, `ticket_status`, `email_templates` also inserted with sample data.
* It will redirect the admin login page.
* In that enter the detail which you added in  `Admin User` tab of wizard and get login.
* Once the product will installed successfully, It will generate one file in `storage` folder name as `installed` with message `App Installer successfully INSTALLED on [Current Date Time]` to insure that the prodcut installed successfully for use.
* If you want to reinstalled it, You should remove the `installed` file from `storage` folder and repeat the previous process again to get it.

