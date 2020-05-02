FROM composer:1.10 AS composer
FROM php:7.4-cli

RUN curl -sL https://deb.nodesource.com/setup_14.x | bash -

RUN apt-get update && apt-get install -y \
    git zip unzip nodejs zlib1g-dev libzip-dev libicu-dev

RUN docker-php-ext-configure intl
RUN docker-php-ext-install zip intl bcmath

COPY --from=composer /usr/bin/composer /usr/bin/composer
