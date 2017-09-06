FROM php:7.0-apache

WORKDIR /var/www/html

#Install dependent software
RUN apt-get update && DEBIAN_FRONTEND=noninteractive apt-get install -y --force-yes \
    cron \
    libreoffice-common \
    libreoffice-draw \
    libreoffice-writer \
    libpng12-dev \
    libjpeg-dev \
    libssl-dev \
    libxml2-dev \
    memcached \
    mysql-client \
    unzip \
    zip

#Install libraries required to compile PHP modules
RUN apt-get update && apt-get install -y --no-install-recommends \
    libaio1 \
    libfreetype6-dev \
    libgd-tools \
    libjpeg62-turbo-dev \
    libmcrypt-dev \
    libmemcached-dev \
    libssh2-1-dev \
    zlib1g-dev


# Install PHP modules
RUN  docker-php-ext-install \
     bcmath \
     calendar \
     exif \
     gd \
     gettext \
     mcrypt \
     mysqli \
     pdo \
     pdo_mysql \
     opcache \
     soap \
     zip

# pecl/stats requires PHP (version >= 5.3.0, version <= 5.6.99), installed version is 7.1.6
#RUN pecl install stats-1.0.5

COPY php.ini /usr/local/etc/php/php.ini
