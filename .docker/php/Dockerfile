FROM php:8.3-fpm

COPY --from=composer /usr/bin/composer /usr/bin/composer

RUN apt update && apt install -y
RUN apt install git -y 
RUN apt install zip unzip -y
RUN docker-php-ext-install pdo pdo_mysql

RUN mv "$PHP_INI_DIR/php.ini-production" "$PHP_INI_DIR/php.ini"
