#changes to include memcache in here
FROM php:7.1-fpm
RUN apt-get update && apt-get install -y \
        libmemcached11 \
        libmemcachedutil2 \
        libmemcached-dev \
        libz-dev \
        git \
    && cd /root \
    && git clone -b php7 https://github.com/php-memcached-dev/php-memcached \
    && cd php-memcached \
    && phpize \
    && ./configure \
    && make \
    && make install \
    && cd .. \
    && rm -rf  php-memcached \
    && echo extension=memcached.so >> /usr/local/etc/php/conf.d/memcached.ini
#    && apt-get autoremove -y \
#    && rm -rf /var/lib/apt/lists/*

# Install Composer for Laravel
RUN curl -sS https://getcomposer.org/installer | php \
    && mv composer.phar /usr/local/bin/composer

#zip is required from Laravel
RUN apt-get install -y zip
