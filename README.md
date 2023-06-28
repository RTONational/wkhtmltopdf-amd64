Description
================

This is a fork of (https://github.com/h4cc/wkhtmltopdf-amd64)[https://github.com/h4cc/wkhtmltopdf-amd64]. Additional documentation for that package (some of which applies to this package) can be found there.

The __h4cc/wkhtmltopdf-amd64__ package is stuck at at wkhtmltopdf version 0.12.4. This was the last wkhtmltopdf release with a generic Linux binary. The intent of this repository is to host the version of the binary actually needed by (Corvus)[https://github.com/RTONational/corvus].


wkhtmltopdf
================

This repository contains the static compiled binaries from the [wkhtmltopdf project](http://wkhtmltopdf.org/).
More about the functionality of wkhtmltopdf and wkthmltoimage can be found there.

## Installation

This forked package is not on Packagist and needs to be installed from GitHub. Add the GitHub repository to the requiring project's composer.json file.

```json
    "repositories": [
        {
            "type": "vcs",
            "url": "https://github.com/RTONational/wkhtmltopdf-amd64"
        }
    ],
```

You cannot load this private repository without special permissions. You will need to create a personal access token for composer.

https://github.com/settings/tokens?type=beta

Generate a new token (I named mine "composer"). Choose the most future expiration date. The resource owner will be `RTO National`. Select "All repositories" under Repository access.

Under the Repository permissions dropdown, change "Contents" to Read-only. Then click the green "Request update" button.

John will need to approve your token.

![image](https://github.com/RTONational/wkhtmltopdf-amd64/assets/6668279/237280f0-8853-4448-b233-ca44073a79c0)

![image](https://github.com/RTONational/wkhtmltopdf-amd64/assets/6668279/ff638376-7c3c-4d66-b06b-c145503b3530)

After this, the package can be installed with

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
