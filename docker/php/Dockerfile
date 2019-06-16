FROM php:7.2-fpm

RUN apt-get update && apt-get install --no-install-recommends -y libpq-dev wget git unzip \
    && pecl install xdebug-2.7.1 \
    && docker-php-ext-enable xdebug \
    && docker-php-ext-install pdo pgsql pdo_pgsql

ADD ./php.ini /usr/local/etc/php/php.ini
ADD ./xdebug.ini /usr/local/etc/php/conf.d/xdebug.ini

RUN wget https://getcomposer.org/installer -O - -q \
    | php -- --install-dir=/bin --filename=composer --quiet

WORKDIR /var/www/html