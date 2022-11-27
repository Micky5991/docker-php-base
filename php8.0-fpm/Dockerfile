FROM nginx:1.23

RUN apt-get update && apt-get -y install apt-transport-https lsb-release ca-certificates wget
RUN wget -O /etc/apt/trusted.gpg.d/php.gpg https://packages.sury.org/php/apt.gpg
RUN sh -c 'echo "deb https://packages.sury.org/php/ $(lsb_release -sc) main" > /etc/apt/sources.list.d/php.list'

RUN apt-get update \
    && apt-get install -y \
    php8.0-fpm \
    php8.0-mysql \
    php8.0-gd \
    php8.0-imagick \
    php8.0-bcmath \
    php8.0-common \
    php8.0-mbstring \
    php8.0-xml \
    php8.0-pdo \
    php8.0-redis \
    php8.0-intl \
    php8.0-curl \
    openssl \
    cron \
    supervisor \
    mariadb-client \
    && rm -rf /var/lib/apt/lists/*

RUN apt-get clean
