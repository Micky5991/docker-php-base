FROM nginx:1.23

RUN apt-get update && apt-get -y install apt-transport-https lsb-release ca-certificates wget
RUN wget -O /etc/apt/trusted.gpg.d/php.gpg https://packages.sury.org/php/apt.gpg
RUN sh -c 'echo "deb https://packages.sury.org/php/ $(lsb_release -sc) main" > /etc/apt/sources.list.d/php.list'

RUN apt-get update \
    && apt-get install -y \
    php8.2-fpm \
    php8.2-mysql \
    php8.2-gd \
    php8.2-imagick \
    php8.2-bcmath \
    php8.2-common \
    php8.2-mbstring \
    php8.2-xml \
    php8.2-pdo \
    php8.2-redis \
    php8.2-intl \
    php8.2-curl \
    openssl \
    cron \
    supervisor \
    mariadb-client \
    libgmp-dev \
    php8.2-gmp \
    ffmpeg \
    python3-pip \
    && rm -rf /var/lib/apt/lists/*

RUN apt-get clean

RUN pip3 install youtube_dl
