# CakePHP Application Skeleton

[![Build Status](https://img.shields.io/travis/cakephp/app/master.svg?style=flat-square)](https://travis-ci.org/cakephp/app)
[![License](https://img.shields.io/packagist/l/cakephp/app.svg?style=flat-square)](https://packagist.org/packages/cakephp/app)

A skeleton for creating applications with [CakePHP](http://u.720life.cn/g/e167901b84c5735c5d9345b9c35ffe71352351db99ec2287c065b601c2f0b497)  3.x.

The framework source code can be found here: [cakephp/cakephp](http://u.720life.cn/g/54145d0471d91890860f7f8463c030465f545a02c0e898ae6477beb551cb6f084aef6eb525ae0f8390cf3dde07dfed43 

## Installation

1. Download [Composer](http://u.720life.cn/g/d5f1cf35647bbcd870aa9cc0452a2958f5b19da47f514ecdb96d246c6524957b397db7acc2c6e4aed124bed1dd69d3b4)  or update `composer self-update`.
2. Run `php composer.phar create-project --prefer-dist cakephp/app [app_name]`.

If Composer is installed globally, run

```bash
composer create-project --prefer-dist cakephp/app
```

In case you want to use a custom app dir name (e.g. `/myapp/`):

```bash
composer create-project --prefer-dist cakephp/app myapp
```

You can now either use your machine's webserver to view the default home page, or start
up the built-in webserver with:

```bash
bin/cake server -p 8765
```

Then visit `http://localhost:8765` to see the welcome page.

## Update

Since this skeleton is a starting point for your application and various files
would have been modified as per your needs, there isn't a way to provide
automated upgrades, so you have to do any updates manually.

## Configuration

Read and edit `config/app.php` and setup the `'Datasources'` and any other
configuration relevant for your application.

## Layout

The app skeleton uses a subset of [Foundation](http://u.720life.cn/g/fda4eb4fcfa6e811af8d9b8b3209ba201e49476215f86342523fcc2b563dec8b)  CSS
framework by default. You can, however, replace it with any other library or
custom styles.



 # 良心友情链接

[腾讯QQ群快速检索](http://u.720life.cn/s/8cf73f7c)

[软件免费开发论坛](http://u.720life.cn/s/bbb01dc0)