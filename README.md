# Laravel Migration

[![License](https://poser.pugx.org/tomzx/laravel-migration/license.svg)](https://packagist.org/packages/tomzx/laravel-migration)
[![Latest Stable Version](https://poser.pugx.org/tomzx/laravel-migration/v/stable.svg)](https://packagist.org/packages/tomzx/laravel-migration)
[![Latest Unstable Version](https://poser.pugx.org/tomzx/laravel-migration/v/unstable.svg)](https://packagist.org/packages/tomzx/laravel-migration)
[![Build Status](https://img.shields.io/travis/tomzx/laravel-migration.svg)](https://travis-ci.org/tomzx/laravel-migration)
[![Code Quality](https://img.shields.io/scrutinizer/g/tomzx/laravel-migration.svg)](https://scrutinizer-ci.com/g/tomzx/laravel-migration/code-structure)
[![Code Coverage](https://img.shields.io/scrutinizer/coverage/g/tomzx/laravel-migration.svg)](https://scrutinizer-ci.com/g/tomzx/laravel-migration)
[![Total Downloads](https://img.shields.io/packagist/dt/tomzx/laravel-migration.svg)](https://packagist.org/packages/tomzx/laravel-migration)

This is a small package that builds on Laravel's wonderful database package. It extracts the database migration feature in order to use it in any project that may not be built on Laravel.

## Note

This is currently a proof of concept. There are rough edges (such as the configuration file and migrations folder location). Those should be fixed given enough time and feedback. Feel free to submit a PR if you have a suggestion on how to deal with those!

This project currently uses some from of "hack" by creating some files in the `Illuminate/Foundation` namespace. It is expected you will not use this project within the context of a Laravel application, otherwise conflicts will occur.

## Getting Started

The current implementation looks for a file `config.php` in the current working directory. Migrations are expected to be in a folder called `migrations`.

```
your-project
- database
-- config.php
-- migrations
--- 2015_11_17_215411_some_migration.php
- vendor
-- tomzx
--- LaravelMigration
```

To use the tool, you would call `laravel-migration` in the following way:

`php ../bin/laravel-migration`

## License

The code is licensed under the [MIT license](http://choosealicense.com/licenses/mit/). See [LICENSE](LICENSE).
