FROM php:5.6-apache
MAINTAINER red <rosso.aquila@gmail.com>

RUN apt-get update \
    && apt-get install -y libmcrypt-dev libfreetype6-dev \
    && a2enmod rewrite \
    && docker-php-ext-install -j$(nproc) iconv mcrypt pdo_mysql

RUN apt-get install -y libjpeg62-turbo-dev libpng12-dev \
	&& docker-php-ext-configure gd --with-freetype-dir=/usr/include/ --with-jpeg-dir=/usr/include/ \
    && docker-php-ext-install -j$(nproc) gd

RUN pecl install xdebug memcache \
    && docker-php-ext-enable xdebug memcache

RUN apt-get install -y libicu-dev \
	&& docker-php-ext-install intl
