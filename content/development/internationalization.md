+++
title= "Internationalization"
date= 2018-02-28T19:42:30+05:30
description = ""
draft= false
weight = 5
+++

RepairRabbit is a multilingual application. it can be run in any language you want and requires less or minimal efforts.

Language strings are stored in files within the `resources/lang` directory. Within this directory there should be a subdirectory for each language supported by the application:

```
/resources
    /lang
        /en
            messages.php
        /es
            messages.php
            
```

All language files return an array of keyed strings. For example:

```
<?php

  return [
      'welcome' => 'Welcome to our application'
  ];
?>
```

#### Change Language Files

If you want to change text. Go to the corresponding language directory and inside language directory go into the file in which you want to change text. After finding the text you can just simply change the text. It will be reflected in application.

<b>Note</b>:- Langauge directory may have multiple language files.


#### Add New Language

If you want to support new language other than english or dutch. Follow the below instruction.

* Create new directory inside `/resources/lang`. Its name must be the `language code` of that language.
* Create exactly same named and number of files as other languages.
* Each files should be identical with other languages. Except value of key. i.e. translations can differ. but the files and keys must be same.
* Now you can add/modify text as you want for each keys.

For example:

You want to add new language `portuguese`.

* Create a directory inside `/resources/lang` called `pt`.
* Create exactly same named and number of files created in other languages. Or Simply can copy all the files and paste in new directory called `pt`.
* Change text with `portuguese` text.

#### Serve In Other Language

* To serve in other language, Change value of `APP_LANGUAGE` in `.env` file to the language code in which you want to serve the application.

For example:

Now you want to serve the application in `portuguese`. So change the value of `APP_LANGUAGE` in `.env` file.

For more details visit this [link](https://laravel.com/docs/5.6/localization)
