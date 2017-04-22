Laravel-Piwik v2.1.3
====================

[![Build Status](https://semaphoreci.com/api/v1/robbrazier/laravel_piwik/branches/master/shields_badge.svg)](https://semaphoreci.com/robbrazier/laravel_piwik)
[![Scrutinizer](https://img.shields.io/scrutinizer/g/robbrazier/laravel_piwik.svg)](https://scrutinizer-ci.com/g/RobBrazier/Laravel_Piwik/?branch=master)
[![Scrutinizer Coverage](https://img.shields.io/scrutinizer/coverage/g/robbrazier/laravel_piwik.svg)](https://scrutinizer-ci.com/g/RobBrazier/Laravel_Piwik/?branch=master)
[![Packagist Version](https://img.shields.io/packagist/v/robbrazier/piwik.svg)](https://packagist.org/packages/robbrazier/piwik)
[![Packagist Total Downloads](https://img.shields.io/packagist/dt/robbrazier/piwik.svg)](https://packagist.org/packages/robbrazier/piwik)
[![Waffle.io](https://img.shields.io/waffle/label/RobBrazier/Laravel_Piwik/in%20progress.svg)](https://waffle.io/RobBrazier/Laravel_Piwik)

An Interface to Piwik's Analytics API for Laravel (Composer Package)

This is the Laravel 5 version of the Laravel-Piwik Bundle.

##Installation

Add `RobBrazier/Piwik` to `composer.json`:

```json
{
    "require": {
        "robbrazier/piwik": "~2.1"
    }
}
```

Add `'RobBrazier\Piwik\PiwikServiceProvider'` and `'Piwik' => 'RobBrazier\Piwik\Facades\Piwik'` to `app/config/app.php`

```php
'providers' = array(
    ...
    'RobBrazier\Piwik\PiwikServiceProvider',
    ...
);

[...]

'aliases' = array(
    ...
    'Piwik' => 'RobBrazier\Piwik\Facades\Piwik',
    ...
);
```

Then move the config file out of the package, so that it doesn't get replaced when you update, by doing `php artisan vendor:publish --provider="RobBrazier\Piwik\PiwikServiceProvider"`.

Update your packages with `composer update` or install with `composer install`.

Then go to `config/piwik.php` and add your config settings such as server, username, password, apikey etc.

##Manual

The Manual is still the same as version 1.0.x, and is at [http://robbrazier.com/projects/laravel-piwik](http://robbrazier.com/projects/laravel-piwik).
