Description
================

This is a fork of (https://github.com/h4cc/wkhtmltopdf-amd64)[https://github.com/h4cc/wkhtmltopdf-amd64]. Additional documentation for that package (some of which applies to this package) can be found there.

The __h4cc/wkhtmltopdf-amd64__ package is stuck at at wkhtmltopdf version 0.12.4. This was the last wkhtmltopdf release with a generic Linux binary. The intent of this repository is to host the version of the binary actually needed by (Corvus)[https://github.com/RTONational/corvus].


wkhtmltopdf
================

This repository contains the static compiled binaries from the [wkhtmltopdf project](http://wkhtmltopdf.org/).
More about the functionality of wkhtmltopdf and wkthmltoimage can be found there.


```
composer require rton/wkhtmltopdf-amd64
```

### Usage

You can use the path constant to easily locate the binary in the PHP codebase:

``` php
$path = \Rton\WKHTMLToPDF\WKHTMLToPDF::PATH;
```

For realpath use following script

``` php
$realpath = realpath(\Rton\WKHTMLToPDF\WKHTMLToPDF::PATH);
```
