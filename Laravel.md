# Laravel Cheat Sheet

Laravel is a free, open-source PHP web application framework, created by Taylor Otwell and intended for the development of web applications following the model–view–controller (MVC) architectural pattern -- [source](https://en.wikipedia.org/wiki/Laravel).

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
Pay attention to where it is installed in the user output that is produced -- it should be somewhere like ...vendor/bin. If you can't
see anything, take a look in a folder which resembles C:\Users\[name]\AppData\Roaming\Composer and you should see the vendor folder
there.

### Installing Gulp
Could be useful :-) Make sure npm and node.js are [installed](https://nodejs.org/en/) first, though.
```
> npm install -g gulp
```

### Creating a new Laravel project
```
> laravel new <project-name>
```

### Asking Artisan for help on a command
```
> php artisan help <command>
e.g.
> php artisan help make:controller
```

### Running a server
```
> php artisan serve
and then go to (usually) http://localhost:8000
```

### Making a migration
```
> php artisan make:migration [name] --create=notes
```
Where name could be something like "create_notes_table" and instead of notes, you would use your table name.

### Running Tinker
```
> php artisan tinker
```

### Making a model
```
> php artisan make:model [name]
```
Where name is the name of the model/class. Add "-m" to make the migration, too.

### Database manipulations in Tinker
```
# show all records - Class::all();
> App\User::all();

# find a record
> App\Note::find(6);

# find AND delete a record
> App\Note::find(6)->delete();
```

### Show full debugging in browser
Go to app\config\app.php and set this line to true:
```
'debug' => env('APP_DEBUG', true),
```

### Faking unimplemented REST methods
```
<form method="POST" action="/notes/{{ $note->id }}">
        {{ method_field('PATCH') }}
```

### Generating a cryptographic key/crypto error
```
> php artisan key:generate
```
In config\app.php, ensure this has the following line:
```
'key' => env('APP_KEY','MF5l...'),
'cipher' => 'AES-256-CBC',
```
Where the MF51 part came from the artisan command above.
This is needed if you see an error like this: 
```
RuntimeException in compiled.php line 7530:
No supported encrypter found. The cipher and / or key length are invalid.
```

### CSRF validation errors
All form elements should use the following:
```
<form....>
        {{ csrf_field() }}
```
Another way, rather like removing a limb to fix an itch, is this: Edit App\Http\Kernel.php as follows:
```
protected $middlewareGroups = [
        'web' => [
            \App\Http\Middleware\EncryptCookies::class,
            \Illuminate\Cookie\Middleware\AddQueuedCookiesToResponse::class,
            \Illuminate\Session\Middleware\StartSession::class,
            \Illuminate\View\Middleware\ShareErrorsFromSession::class,
           //  \App\Http\Middleware\VerifyCsrfToken::class,
```
Although this absolutely isn't the *right* way :-)

### Resources
* [Documentation](https://laravel.com/docs/5.2)
* [Videos](https://laracasts.com/)
* [Jeffrey Way's GitHub Repo](https://github.com/JeffreyWay?tab=repositories)
* [Other Resources](http://codecondo.com/laravel-news-resources-tutorials/)

Written by Stephen Moon stephen@logicalmoon.com, 2016
