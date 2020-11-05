FROM php:5.6.29-fpm
RUN apt-get update && apt-get install -y unzip libpng-dev libcurl4-gnutls-dev libxml2-dev libzip-dev && CFLAGS="-I/usr/src/php"
RUN pecl channel-update pecl.php.net
RUN docker-php-ext-install gd zip curl mbstring
RUN docker-php-ext-install mysqli mysql soap opcache
RUN docker-php-ext-install pdo pdo_mysql
RUN pecl install xdebug-2.5.5
RUN apt-get update && apt-get install -y git
