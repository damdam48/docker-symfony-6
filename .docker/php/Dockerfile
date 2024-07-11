FROM php:8.3-fpm

COPY --from=composer /usr/bin/composer /usr/bin/composer

RUN apt update && apt install
RUN apt install zip unzip
RUN docker-php-ext-install pdo pdo_mysql

RUN mv "$PHP_INI_DIR/php.ini-production" "$PHP_INI_DIR/php.ini"
