+++
title= "Use product default"
date= 2018-01-18T19:42:30+05:30
description = ""
draft= true
+++

## Prerequisites

* [Laravel 5.4](http://laravel.com/)
* [MySQL] (https://www.mysql.com/downloads/)
* [Valet] (https://laravel.com/docs/5.4/valet)

## Setup

Install project

```
git clone git@gitlab.com:improwised/phoneworld.git
```

Link that folder in valet using

```
valet link folder_name
```

Goto the following path to install the product
```
http://folder.dev/install
```

Once the product will installed, It redirects the home route at user side to access the admin side go to /admin in url.

Successfully Installation creates one ```installed``` file in storage folder to track that the product was installed or not, after installation if you want to reinstall the product you should remove that ```installed``` file from storage folder.

