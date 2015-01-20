Caffeinated Flash Messages
==========================
[![Laravel](https://img.shields.io/badge/Laravel-5.0-orange.svg?style=flat-square)](http://laravel.com)
[![Source](http://img.shields.io/badge/source-caffeinated/flash-blue.svg?style=flat-square)](https://github.com/caffeinated/flash)
[![Build Status](http://img.shields.io/travis/caffeinated/flash/master.svg?style=flat-square)](https://travis-ci.org/caffeinated/flash)
[![Scrutinizer Code Quality](http://img.shields.io/scrutinizer/g/caffeinated/flash.svg?style=flat-square)](https://scrutinizer-ci.com/g/caffeinated/flash/?branch=master)
[![Scrutinizer Code Coverage](https://img.shields.io/scrutinizer/coverage/g/caffeinated/flash.svg?style=flat-square)](https://scrutinizer-ci.com/g/caffeinated/flash/?branch=master)
[![License](http://img.shields.io/badge/license-MIT-brightgreen.svg?style=flat-square)](https://tldrlegal.com/license/mit-license)

Laravel 5 flash messages, originally developed after the Laracasts video tutorial on the same topic: [Flexible Flash Messages](https://laracasts.com/lessons/flexible-flash-messages).

Installation
------------
Begin by installing the package through Composer. The best way to do this is through your terminal via Composer itself:

```
composer require caffeinated/flash
```

Once this operation is complete, simply add both the service provider and facade classes to your project's `config/app.php` file:

#### Service Provider
```
'Caffeinated\Flash\FlashServiceProvider'
```

#### Facade
```
'Flash' => 'Caffeinated\Flash\Facades\Flash'
```

And that's it! With your coffee in reach, start flashing out messages!

Usage
-----
Usage is simple. Before redirecting to another page, simply call on `Flash` to set your desired flash message. There are a number of methods to assign different levels of priority (info, success, warning, and error).

#### Success

```php
Flash::success('This is a success message.');
```

#### Info

```php
Flash::info('This is an info message.');
```

#### Warning

```php
Flash::warning('This is a warning message.');
```

#### Error

```php
Flash::error('This is an error message.');
```

### Rendering
To render your flash messages in your view, simply include the bundled view partial in your master layout:

```php
@include('flash::message')
```

Note that the bundled view partial is geared for Bootstrap out of the box.
