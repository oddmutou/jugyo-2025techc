FROM php:8.4-fpm-alpine AS php

RUN apk add -U --no-cache curl-dev
RUN docker-php-ext-install curl
RUN docker-php-ext-install exif

RUN apk add autoconf g++ make
RUN pecl install apcu && docker-php-ext-enable apcu

RUN apk add libpng-dev
RUN docker-php-ext-install gd
