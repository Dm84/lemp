FROM php:7.3.2-fpm
RUN apt-get update && apt-get install -y libcurl4-gnutls-dev && docker-php-ext-install curl mbstring mysqli && pecl install xdebug