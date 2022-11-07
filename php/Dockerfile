FROM php:8.0-apache

COPY ./php.ini /usr/local/etc/php
COPY ./apache2.conf /etc/apache2/conf-enabled
COPY ./mod_perl.conf /etc/apache2/conf-enabled

RUN apt-get update \
  && apt-get install -y libfreetype6-dev libjpeg62-turbo-dev libpng-dev libmcrypt-dev vim perl libdbi-perl libdbd-mysql libhtml-template-compiled-perl libcgi-simple-perl libcgi-session-perl libapache2-mod-perl2 \
  && docker-php-ext-install mysqli pdo_mysql gd

RUN a2enmod rewrite
