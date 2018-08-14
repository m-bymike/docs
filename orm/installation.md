# Installation in Laravel 5+

 Laravel  | Laravel Doctrine
:---------|:----------
 5.1.*    | 1.0.*
 5.2.*    | 1.1.*
 5.3.*    | 1.2.*
 5.4.*    | 1.3.*
 5.5.*    | 1.4.*
 5.6.*    | 1.4.*

Install this package with composer:

```
composer require "laravel-doctrine/orm:1.4.*"
```

To publish the config use:

```php
php artisan vendor:publish --provider="LaravelDoctrine\ORM\DoctrineServiceProvider"
```

Available environment variables inside the config are: `APP_DEBUG`, `DOCTRINE_METADATA`, `DB_CONNECTION`, `DOCTRINE_PROXY_AUTOGENERATE`, `DOCTRINE_LOGGER` and `DOCTRINE_CACHE`

> Important:
> By default, Laravel's application skeleton has its `Model` classes in the `app/` folder. With Doctrine, you'll need to
> create a dedicated folder for your `Entities` and point your `config/doctrine.php` `paths` array to it.
> If you don't, Doctrine will scan your whole `app/` folder for files, which will have a huge impact on performance!
>
> ```
> 'paths' => [
>     base_path('app/Entities'),
> ],
> ```
