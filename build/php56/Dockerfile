FROM php:5.6.29-fpm
RUN CFLAGS="-I/usr/src/php"
RUN apt-get update && apt-get install -y unzip libpng-dev libcurl4-gnutls-dev libxml2-dev libzip-dev
RUN pecl channel-update pecl.php.net
RUN docker-php-ext-install zip curl mbstring
RUN docker-php-ext-install mysqli mysql soap opcache
RUN docker-php-ext-install pdo pdo_mysql
RUN apt-get update && apt-get install -y git
RUN curl -s https://getcomposer.org/installer | php && mv composer.phar /usr/local/bin/composer
RUN apt-get install -y libxslt-dev && CFLAGS="-I/usr/src/php"
RUN docker-php-ext-install exif iconv json simplexml xsl
RUN pecl install xdebug-2.5.5
RUN apt-get install -y libjpeg-dev libfreetype6-dev libonig-dev
RUN docker-php-ext-configure gd \
        -with-png-dir=/usr --with-jpeg-dir=/usr \
        --with-freetype \
        --with-jpeg
RUN docker-php-ext-install gd


