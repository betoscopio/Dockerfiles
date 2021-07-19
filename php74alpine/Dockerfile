FROM php:7.4-fpm-alpine

# Inspired by https://stackoverflow.com/questions/61228386/installing-gd-extension-in-docker
# https://www.programmersought.com/article/37695330408/

# May need some dependencies https://github.com/docker-library/php/issues/326
# use https://pkgs.alpinelinux.org/contents?file=icu-config&branch=v3.4&arch=x86_64 to search required files

RUN apk update && \
    apk add --update-cache --no-cache freetype-dev \
    gettext-dev \
#   icu-dev \
    jpeg-dev \
    libpng-dev \
    libzip-dev \
    zlib-dev

RUN docker-php-ext-configure gd --with-freetype --with-jpeg \
 && docker-php-ext-configure opcache --enable-opcache \
 && docker-php-ext-install -j$(nproc) gd \
 bcmath \
 calendar \
 exif \
 gettext \
# intl
# mysqli \
# pcntl \
# shmop \
# sysvmsg
# sockets \
# xsl \
 opcache \
 pdo_mysql \
 zip \
 && rm -rf /var/cache/apk/*

CMD ["php-fpm"]

EXPOSE 9000
