---
title: Getting php.ini and and php-cli to play nice on nitrous.io
categories:
    - php
    - php cli
    - php.ini
    - nitrous.io
---
I was having trouble getting nitrous.io to read my php.ini settings - it looks like it doesn't pick up on the one in the apache dir.
I ended up having to invoke it like this:

~~~bash
php -c /home/action/.parts/etc/php5/php.ini /home/action/.parts/bin/sculpin generate --watch --server
~~~

Relevant Links
==============
http://stackoverflow.com/questions/12108207/php-date-timezone-not-working-correctly-for-command-line-script-only

https://github.com/nitrous-io/autoparts/issues/110