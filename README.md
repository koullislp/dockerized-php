# dockerized-php
A docker project that includes php (5 and 7) with memcache extensions, a memcached server and redis server

Thanks to the GeekPlatypus for his code on PHP-FPM and integrating NginX using Docker Compose
http://geekyplatypus.com/dockerise-your-php-application-with-nginx-and-php7-fpm/

#Requirements
- docker
- docker-compose (version 3)

#Executing
- pick a directory to run in according to the PHP version of your preference
- $ docker-compose up -d
- the above command will launch an NginX webserver, a PHP environment attached to NginX, a Memcached server as well as a Redis server
