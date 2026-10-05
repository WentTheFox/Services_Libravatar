# Services_Libravatar
A PHP 8.4+ library to the `Libravatar <https://www.libravatar.org/>`_ service
that delivers avatar pictures to other websites:
It gives you image URLs for email addresses.

Forked from https://github.com/pear/Services_Libravatar

## Installation

Via Composer:

```bash
$ composer require wentthefox/services_libravatar
```

## Usage

```php
<?php

require 'vendor/autoload.php';

use PEAR\Services\Libravatar;

$emailOrHash = 'test@example.com';
# OR $emailOrHash = '55502f40dc8b7c769880b10874abc9d0';

$service = new Libravatar();
$service->setHttps(true);
$service->setSize(128);
echo $service->getUrl($emailOrHash);
# https://seccdn.libravatar.org/avatar/55502f40dc8b7c769880b10874abc9d0?size=128
```

Additional documentation available at the [original source](https://pear.php.net/manual/en/package.webservices.services-libravatar.basic.php). Most methods signatures are identical.
