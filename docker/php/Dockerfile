FROM php:7.2-fpm

RUN apt-get update && apt-get install -y \
        curl \
        wget \
        git \
        libfreetype6-dev \
        libjpeg62-turbo-dev \
        libmcrypt-dev \
        libpq-dev \
        libzip-dev  \
        libicu-dev

# PHP Extensions
RUN docker-php-ext-install -j$(nproc) iconv mbstring mysqli pdo_mysql zip pdo_pgsql pgsql \
&& docker-php-ext-install -j$(nproc) gd \
&& pecl install xdebug \
&& docker-php-ext-enable xdebug

# Memory Limit
RUN echo "memory_limit=1024M" > $PHP_INI_DIR/conf.d/memory-limit.ini
RUN echo "max_execution_time=900" >> $PHP_INI_DIR/conf.d/memory-limit.ini
RUN echo "post_max_size=20M" >> $PHP_INI_DIR/conf.d/memory-limit.ini
RUN echo "upload_max_filesize=20M" >> $PHP_INI_DIR/conf.d/memory-limit.ini

# Time Zone
RUN echo "date.timezone=${PHP_TIMEZONE:-UTC}" > $PHP_INI_DIR/conf.d/date_timezone.ini

# Display errors
RUN echo "display_errors=On" > $PHP_INI_DIR/conf.d/display-errors.ini

# Install Composer
RUN curl -sS https://getcomposer.org/installer | php -- --install-dir=/usr/local/bin --filename=composer

RUN usermod -u 1000 www-data

EXPOSE 9000
CMD ["php-fpm"]