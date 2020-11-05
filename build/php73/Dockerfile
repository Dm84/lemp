FROM php:7.3.2-fpm

RUN apt-get update && apt-get install -y unzip libpng-dev libcurl4-gnutls-dev libxml2-dev libzip-dev libxslt-dev
RUN apt-get install -y libjpeg-dev libfreetype6-dev
RUN CFLAGS="-I/usr/src/php"
RUN docker-php-ext-configure gd \
        --with-freetype-dir=/usr/lib/ \
        --with-png-dir=/usr/lib/ \
        --with-jpeg-dir=/usr/lib/ \
        --with-gd
RUN docker-php-ext-install gd zip curl
RUN docker-php-ext-install mbstring mysqli soap opcache
RUN docker-php-ext-install pdo_mysql bcmath intl xsl
RUN docker-php-ext-install sockets
RUN pecl install xdebug
RUN curl -s https://getcomposer.org/installer | php && mv composer.phar /usr/local/bin/composer
RUN apt-get update && apt-get install -y git
