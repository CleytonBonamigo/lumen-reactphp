# Lumen-reactphp
ReactPHP Server on Lumen 5.2, basically a fork of [nazo/laravel-reactphp](https://github.com/nazo/laravel-reactphp), but changed for work with Lumen 5.2.

- Install via composer

```sh
composer require cleytonbonamigo/lumen-reactphp
```

- After installing, add provider on bootstrap/app.php on your project.

```php
// app.php
    $app->register(LaravelReactPHP\Providers\ReactCommandProvider::class); 
```

- By default, Lumen 5.2 removes some app facades, so, you need to re add on bootstrap/app.php
```php
// app.php
	class_alias('Illuminate\Support\Facades\App', 'App');
	class_alias('Illuminate\Support\Facades\Request', 'Request');
```

## Run server

```sh
php artisan react-serve
```