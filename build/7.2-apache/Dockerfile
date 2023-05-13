FROM mobtitude/php-xdebug:7.2-apache

COPY sources.list /etc/apt/sources.list

RUN apt-get update && apt-get install -y \
    libbz2-dev

RUN docker-php-ext-install bz2

COPY xdebug2.ini /usr/local/etc/php/conf.d/xdebug.ini
COPY php.ini /usr/local/etc/php/php.ini

# docker build -t dummykitty/php-xdebug:7.2-apache .