FROM nginx:1.23

RUN apt-get update && apt-get -y install apt-transport-https lsb-release ca-certificates wget
RUN wget -O /etc/apt/trusted.gpg.d/php.gpg https://packages.sury.org/php/apt.gpg
RUN sh -c 'echo "deb https://packages.sury.org/php/ $(lsb_release -sc) main" > /etc/apt/sources.list.d/php.list'

RUN apt-get update \
    && apt-get install -y \
    php8.1-fpm \
    php8.1-mysql \
    php8.1-gd \
    php8.1-imagick \
    php8.1-bcmath \
    php8.1-common \
    php8.1-mbstring \
    php8.1-xml \
    php8.1-pdo \
    php8.1-redis \
    php8.1-intl \
    php8.1-curl \
    openssl \
    cron \
    supervisor \
    mariadb-client \
    && rm -rf /var/lib/apt/lists/*

RUN apt-get clean
