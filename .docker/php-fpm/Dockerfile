FROM php:7.4-fpm-alpine3.13

RUN apk update && apk upgrade
RUN apk add --no-cache bash
RUN apk add zip libzip-dev gnupg

RUN docker-php-ext-install zip pdo_mysql
