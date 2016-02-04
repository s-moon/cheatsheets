# Laravel Cheat Sheet

Laravel is -- [source](link).

###Pre-requisites
* Make sure you have installed PHP version >= 5.5.9
* You should also have OpenSSL PHP, PDP PHP, Mbstring PHP and Tokenizer PHP extensions but these might come anyway.

### Installing Composer
Using this makes it much easier to install the remaining components. Go [here](https://getcomposer.org/download/) and choose the
installer that matches your system. Once installed, check it is working with:
```
> composer
```

### Installing Laravel
This only needs to be run once.
```
> composer global require "laravel/installer"
```
Now add this to your path. Pay attention to where it is installed in the user output that is produced -- it
should be somewhere like ...vendor/bin.

### Creating a new Laravel Project
```
> laravel new <project-name>
```

### Asking artisan for help on a command
```
> php artisan help <command>
e.g.
> php artisan help make:controller
```

Written by Stephen Moon stephen@logicalmoon.com, 2016
