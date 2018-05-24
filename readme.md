SessionHandlerRedis
===================

PHP Session Handler module for ProcessWire that uses Redis as the back-end storage engine.


The Need
--------

Using Redis as the back-end storage engine allows you to store your session data in the memory of a dedicated or shared
redis server. This allows sessions to be shared across multiple front-end instances of ProcessWire.


Config
------

By default the module will attempt to connect to redis on 127.0.0.1 using the default redis port of 6379. It will use
a TTL of 30 mins (1800seconds) for all session keys and will prefix them with PHPSESSID: and store them all in the
default redis DB (number 0).

You can change any of these defaults by adding the following lines to your config.php file (adjusting as needed)...

    $config->redis_session_server_ip     = '127.0.0.1';
    $config->redis_session_server_port   = 6379;
    $config->redis_session_server_db     = 0;
    $config->redis_session_server_prefix = "PHPSESSID:";
    $config->redis_session_server_ttl    = 1800;


License
-------

GPLv2+
