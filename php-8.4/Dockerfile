FROM php:8.4-fpm

ADD https://github.com/mlocati/docker-php-extension-installer/releases/latest/download/install-php-extensions /usr/local/bin/

RUN apt-get update && \
    apt-get install -y locales && \
    apt-get clean && \
    sed -i -e 's/# en_US.UTF-8 UTF-8/en_US.UTF-8 UTF-8/' /etc/locale.gen && \
    dpkg-reconfigure --frontend=noninteractive locales

# https://github.com/mlocati/docker-php-extension-installer
RUN chmod uga+x /usr/local/bin/install-php-extensions \
    && sync \
    && install-php-extensions \
        apcu \
        bcmath \
        calendar \
        decimal \
        excimer \
        exif \
        gd \
        gettext \
        gmp \
        grpc \
        igbinary \
        imap \
        intl \
        mailparse \
        opcache \
        pcntl \
        pdo_mysql \
        protobuf \
        redis \
        soap \
        ssh2 \
        xsl \
        yaml \
        zip \
    && mv "$PHP_INI_DIR/php.ini-production" "$PHP_INI_DIR/php.ini"

ENV LANG en_US.UTF-8
ENV LANGUAGE en_US:en
ENV LC_ALL en_US.UTF-8
