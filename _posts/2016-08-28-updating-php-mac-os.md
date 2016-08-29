---
layout: post
title: Updating PHP Mac OS X El Capitan
subtitle: Troubleshooting PHP Update, by José Simán
---
As of today, Mac OS X El Capitan comes pre loaded with PHP 5.5.36.

php is located in /usr/bin/

```php -v``` outputs:

```bash
PHP 5.5.36 (cli) (built: May 29 2016 01:07:06)
Copyright (c) 1997-2015 The PHP Group
Zend Engine v2.5.0, Copyright (c) 1998-2015 Zend Technologies
```

The easiest way to update to PHP 5.6 is to open the Terminal and type:

```curl -s http://php-osx.liip.ch/install.sh | bash -s 5.6
```

However, it may happen to you that after the update, ```php -v``` does not display PHP 5.6.  This is because you still need to update your PATH to the directory where PHP was placed, which is /usr/local/php5/bin/php

To do so, open Terminal and edit your .bash_profile file and add these lines to it:

```bash
PATH="/usr/local/php5/bin:${PATH}"
export PATH
```

Exit Terminal and open it again and now type ```php -v```  now you should see something like this:

```bash
PHP 5.6.23 (cli) (built: Jun 26 2016 13:17:47)
Copyright (c) 1997-2016 The PHP Group
Zend Engine v2.6.0, Copyright (c) 1998-2016 Zend Technologies
    with Zend OPcache v7.0.6-dev, Copyright (c) 1999-2016, by Zend Technologies
    with Xdebug v2.2.5, Copyright (c) 2002-2014, by Derick Rethans
```