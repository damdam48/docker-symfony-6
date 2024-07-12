FROM php:8.3-fpm

COPY --from=composer /usr/bin/composer /usr/bin/composer

RUN apt-get update && apt-get install -y \
    zip \
    unzip \
    git \
    curl \
    && docker-php-ext-install pdo pdo_mysql zip gd

RUN mv "$PHP_INI_DIR/php.ini-production" "$PHP_INI_DIR/php.ini"
