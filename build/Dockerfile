FROM php:7.3.2-fpm
RUN apt-get update && apt-get install -y libcurl4-gnutls-dev libxml2-dev && docker-php-ext-install curl mbstring mysqli soap opcache && pecl install xdebug
