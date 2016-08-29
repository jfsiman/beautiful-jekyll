---
layout: post
title: Updating PHP Mac OS X El Capitan
subtitle: Troubleshooting PHP Update, by José Simán
---
As of today, Mac OS X El Capitan comes pre loaded with PHP 5.5.36.

php is located in /usr/bin/

```php -v outputs:```

~~~~
HP 5.5.36 (cli) (built: May 29 2016 01:07:06)
Copyright (c) 1997-2015 The PHP Group
Zend Engine v2.5.0, Copyright (c) 1998-2015 Zend Technologies
~~~~

The easiest way to update to PHP 5.6 is to open the Terminal and type:

```curl -s http://php-osx.liip.ch/install.sh | bash -s 5.6
```


