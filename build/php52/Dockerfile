FROM php:5.6.29-fpm
RUN apt-get update && apt-get install -y unzip libpng-dev libcurl4-gnutls-dev libxml2-dev libzip-dev && CFLAGS="-I/usr/src/php"
RUN pecl channel-update pecl.php.net
RUN docker-php-ext-install gd zip curl mbstring mysqli soap opcache
RUN pecl install xdebug-2.5.5
