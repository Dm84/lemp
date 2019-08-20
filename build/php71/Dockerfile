FROM php:7.1.29-fpm
RUN apt-get update && apt-get install -y unzip libpng-dev libcurl4-gnutls-dev libxml2-dev libzip-dev && CFLAGS="-I/usr/src/php" docker-php-ext-install gd zip curl mbstring mysqli soap opcache && pecl install xdebug && curl -s https://getcomposer.org/installer | php && mv composer.phar /usr/local/bin/composer
