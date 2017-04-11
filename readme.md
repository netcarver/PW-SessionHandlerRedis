SessionHandlerRedis
===================

PHP Session Handler module for ProcessWire that uses Redis as the back-end storage engine.


The Need
--------

Using Redis as the back-end storage engine allows you to store your session data in the memory of a dedicated or shared
redis server. This allows sessions to be shared across multiple front-end instances of ProcessWire.

Prerequisite
-----------

1. Installed Redis on local.
2. Installed phpredis on local.

Config
------

By default the module will attempt to connect to redis on 127.0.0.1 using the default redis port of 6379. It will use
a TTL of 30 mins (1800seconds) for all session keys and will prefix them with PHPSESSID: and store them all in the
default redis DB (number 0).

You can change any of these defaults using module configuration.


License
-------

GPLv2+
