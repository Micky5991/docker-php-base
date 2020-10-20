FROM micky5991/docker-php-base:php7.4-fpm

RUN apt-get update && apt-get -y install apt-transport-https lsb-release ca-certificates wget
RUN wget -O /etc/apt/trusted.gpg.d/php.gpg https://packages.sury.org/php/apt.gpg
RUN sh -c 'echo "deb https://packages.sury.org/php/ $(lsb_release -sc) main" > /etc/apt/sources.list.d/php.list'

RUN apt-get update \
    && apt-get install -y \
    libgmp-dev \
    php7.4-gmp \
    ffmpeg \
    python3-pip \
    && rm -rf /var/lib/apt/lists/*

RUN apt-get clean

RUN pip3 install youtube-dl
