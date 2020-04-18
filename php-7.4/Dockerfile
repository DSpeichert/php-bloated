FROM php:7.4-fpm

ADD https://raw.githubusercontent.com/mlocati/docker-php-extension-installer/master/install-php-extensions /usr/local/bin/

RUN chmod uga+x /usr/local/bin/install-php-extensions \
    && sync \
    && install-php-extensions \
        apcu \
        bcmath \
        decimal \
        gd \
        grpc \
        igbinary \
        imap \
        intl \
        mailparse \
        mcrypt \
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
