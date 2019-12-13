FROM php:7.3.2-fpm
RUN apt-get update && apt-get install -y unzip libpng-dev libcurl4-gnutls-dev libxml2-dev libzip-dev
RUN docker-php-ext-install curl mbstring
RUN docker-php-ext-install mysqli soap opcache
RUN docker-php-ext-install gd zip
RUN pecl install xdebug
