# Lingo

[![Latest Stable Version](https://img.shields.io/packagist/v/ctf0/lingo.svg)](https://packagist.org/packages/ctf0/lingo) [![Total Downloads](https://img.shields.io/packagist/dt/ctf0/lingo.svg)](https://packagist.org/packages/ctf0/lingo)
[![Donate with Bitcoin](https://en.cryptobadges.io/badge/micro/16ri7Hh848bw7vxbEevKHFuHXLmsV8Vc9L)](https://en.cryptobadges.io/donate/16ri7Hh848bw7vxbEevKHFuHXLmsV8Vc9L)

A file based translation manager, which unlike other Lang managers don't need a database connection to handle the translation.

<p align="center">
    <img src="https://user-images.githubusercontent.com/7388088/36597526-11d85cdc-18b2-11e8-8036-38d716e9ef2c.png">
</p>

<br>

## Installation

- `composer require ctf0/lingo`

- (Laravel < 5.5) add the service provider

    ```php
    'providers' => [
        ctf0\Lingo\LingoServiceProvider::class,
    ]
    ```

- publish the package assets with

    `php artisan vendor:publish --provider="ctf0\Lingo\LingoServiceProvider"`

- after installation, package will auto-add
    + package routes to `routes/web.php`
    + package assets compiling to `webpack.mix.js`

- install dependencies

    ```bash
    yarn add vue axios vue-ls vue-notif vue-clipboard2 vue-tippy@v1 vue-awesome@v2
    # or
    npm install vue axios vue-ls vue-notif vue-clipboard2 vue-tippy@v1 vue-awesome@v2 --save
    ```

- add this one liner to your main js file and run `npm run watch` to compile your `js/css` files.
    - if you are having issues [Check](https://ctf0.wordpress.com/2017/09/12/laravel-mix-es6/)

    ```js
    require('../vendor/Lingo/js/manager')

    new Vue({
        el: '#app'
    })
    ```

<br>

## Features

- filter by keys.
- add/remove "vendor/locale/file/item".
- show guiding steps while adding new vendor for better UX.
- validate for "vendor/locale/file" existence on the fly.
- use localeStorage to remember opened "tab/vendor/files/copy-format".
- support up to 3 levels deep on nested keys.
- support all laravel different translation key formats.
- directly copy translation key by clicking on the tool-tip.
- show/hide different elements to avoid noise & keep the user focused.
- copy/paste items.
- merge multiple items under new key.

<br>

## Usage

- visit `localhost:8000/lingo`