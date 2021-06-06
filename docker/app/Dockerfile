FROM php:7.4-fpm

COPY . /var/www/html
COPY --from=composer:1.10 /usr/bin/composer /usr/bin/composer

RUN apt-get update \
&& apt-get install -y \
git \
zip \
unzip \
&& docker-php-ext-install pdo_mysql bcmath

WORKDIR /var/www/html