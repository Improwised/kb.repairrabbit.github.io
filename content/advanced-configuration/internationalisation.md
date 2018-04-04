+++
title= "internationalisation"
date= 2018-02-28T19:42:30+05:30
description = ""
draft= true
weight = 5
+++

RepairRabbit is a multilingual application. Currently, RepairRabbit supports two languages english and dutch by default.

Language files are written inside `resource/lang` directory.

All language files return an array of keyed strings. For example:


#### Serve In Other Language

* To serve in other language, Change value of `APP_LANGUAGE` in `.env` file to the language code in which you want to serve the application.

For example:

Now you want to serve the application in `da`. So change the value of `APP_LANGUAGE` to `da` in `.env` file.

For more details visit this [link](https://laravel.com/docs/5.4/localization)
