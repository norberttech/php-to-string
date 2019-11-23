# PHP To String

Simple library that converts PHP values into strings.

Status: 

* ![Build Status](https://github.com/coduo/php-to-string/workflows/Tests/badge.svg?branch=master) - master


Simple library that allows you to cast any php value into string

## Installation

```
composer require coduo/php-to-string
```

## Usage

Supported types:

* string
* integer
* float/double
* object
* callable
* array
* resource

```php
use Coduo\ToString\StringConverter;

$double = new StringConverter(1.12312);
echo $double; // "1.12312"

$datetime = new StringConverter(new \DateTime());
echo $datetime; // "\DateTime"

$array = new StringConverter(array('foo', 'bar', 'baz'));
echo $array; // "Array(3)"

$res = fopen(sys_get_temp_dir() . "/foo", "w");
$resource = new StringConverter($res);
echo $resource; // "Resource(stream)"

```
