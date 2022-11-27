FROM composer:2.4 AS composer
FROM php:7.4-cli

RUN curl -sL https://deb.nodesource.com/setup_16.x | bash -

RUN apt-get update \
    && apt-get install -y git zip unzip nodejs zlib1g-dev libzip-dev libicu-dev libgmp-dev \
    && rm -rf /var/lib/apt/lists/* \
    && apt-get clean

RUN docker-php-ext-configure intl
RUN docker-php-ext-install zip intl bcmath gmp pcntl

COPY --from=composer /usr/bin/composer /usr/bin/composer
