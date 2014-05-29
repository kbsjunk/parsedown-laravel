Parsedown Extra for Laravel
=====================

A Parsedown Extra wrapper for Laravel to compile markdown to HTML.

[Parsedown](http://parsedown.org/) is fast and supports GitHub flavored markdown.
[Parsedown Extra](https://github.com/erusev/parsedown-extra) adds support for [Markdown Extra](http://en.wikipedia.org/wiki/Markdown_Extra).

Installation
------------

require package in `composer.json`

```json
"require": {
	"laravel/framework": "4.1.*",
	"maxhoffmann/parsedown-laravel": "dev-master"
},
```

add parsedown’s service provider in `config/app.php`

```php
'providers' => array(

	'Illuminate\Foundation\Providers\ArtisanServiceProvider',
	...
	'Illuminate\Workbench\WorkbenchServiceProvider',

	'MaxHoffmann\Parsedown\ParsedownServiceProvider'
),
```

and parsedown’s facade (also in `config/app.php`)

```php
'aliases' => array(

	'App'             => 'Illuminate\Support\Facades\App',
	...
	'View'            => 'Illuminate\Support\Facades\View',

	'Markdown'        => 'MaxHoffmann\Parsedown\ParsedownFacade',

),
```

Usage
-----

```php
Markdown::parse('__Hello__ Markdown!');
// returns '<p><strong>Hello</strong> Markdown!</p>'
```
