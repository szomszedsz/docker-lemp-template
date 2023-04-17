FROM php:8.2-fpm
RUN apt-get update && apt-get install -y \
    git \
    unzip \
    libzip-dev \
    && docker-php-ext-install zip \
    && pecl install xdebug \
    && docker-php-ext-enable xdebug
COPY ./.docker/php/conf.d/xdebug.ini /usr/local/etc/php/conf.d/xdebug.ini
WORKDIR /var/www/html