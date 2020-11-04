FROM php:7.4-fpm

RUN apt-get update && apt-get install -y unzip libpng-dev libcurl4-gnutls-dev libxml2-dev libzip-dev libxslt-dev
RUN apt-get install -y libjpeg-dev libfreetype6-dev libonig-dev
RUN CFLAGS="-I/usr/src/php"
RUN docker-php-ext-configure gd \
        --with-freetype \
        --with-jpeg
RUN docker-php-ext-install gd zip curl
RUN docker-php-ext-install mbstring mysqli soap opcache
RUN docker-php-ext-install pdo_mysql bcmath intl xsl
RUN docker-php-ext-install sockets exif
RUN pecl install xdebug
RUN curl -s https://getcomposer.org/installer | php && mv composer.phar /usr/local/bin/composer

