# ZURB Foundation Bundle for Symfony Framework

## Installation

### Add bundle to your composer.json file

``` js
// composer.json

{
    "require": {
		// ...
        "itlized/zurb-foundation": "dev-master"
    }
}
```

### Add bundle to your application kernel

``` php
// app/AppKernel.php

public function registerBundles()
{
    $bundles = array(
        // ...
        new Itlized\Bundle\ZurbFoundationBundle\ItlizedZurbFoundationBundle(),
        // ...
    );
}
```

### Download the bundle using Composer

``` bash
$ php composer.phar update itlized/zurb-foundation
```

### Install assets

Given your server's public directory is named "web", install the public vendor resources

``` bash
$ php app/console assets:install web
```

Optionally, use the --symlink attribute to create links rather than copies of the resources

``` bash
$ php app/console assets:install --symlink web
```

## Usage

Refer to the desired files in your HTML template, e.g.

``` html
<link rel="stylesheet" type="text/css" href="{{ asset('bundles/itlizedzurbfoundation/css/foundation.min.css') }}" />
```

The Foundation scripts requires jQuery. The bundle installs itlized/zurb-foundation, which should be referenced before
loading any foundation script.

``` html
<script type="text/javascript" src="{{ asset('bundles/itlizedzurbfoundation/js/vendor/jquery.js') }}"></script>
<script type="text/javascript" src="{{ asset('bundles/itlizedzurbfoundation/js/foundation.min.js') }}"></script>
```

## Licenses

Zurb Foundation is MIT licensed

## References

1. http://foundation.zurb.com
2. http://symfony.com
3. http://itlized.com