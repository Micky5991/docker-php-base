FROM nginx:1.23

RUN apt-get update && apt-get -y install apt-transport-https lsb-release ca-certificates wget
RUN wget -O /etc/apt/trusted.gpg.d/php.gpg https://packages.sury.org/php/apt.gpg
RUN sh -c 'echo "deb https://packages.sury.org/php/ $(lsb_release -sc) main" > /etc/apt/sources.list.d/php.list'

RUN apt-get update \
    && apt-get install -y \
    php7.4-fpm \
    php7.4-mysql \
    php7.4-gd \
    php7.4-imagick \
    php7.4-bcmath \
    php7.4-json \
    php7.4-common \
    php7.4-mbstring \
    php7.4-xml \
    php7.4-pdo \
    php7.4-redis \
    php7.4-intl \
    php7.4-curl \
    openssl \
    cron \
    supervisor \
    mariadb-client \
    libgmp-dev \
    php7.4-gmp \
    ffmpeg \
    python3-pip \
    && rm -rf /var/lib/apt/lists/*

RUN apt-get clean

RUN pip3 install youtube_dl
