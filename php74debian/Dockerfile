FROM php:7.4-fpm

# Inspired by https://stackoverflow.com/questions/61228386/installing-gd-extension-in-docker
# https://www.programmersought.com/article/37695330408/


RUN apt-get update && \
    apt-get install -y \
    libfreetype6-dev \
    libjpeg62-turbo-dev \
    libpng-dev \
    libzip-dev

RUN docker-php-ext-install -j$(nproc) iconv \
    && docker-php-ext-configure gd --with-freetype --with-jpeg \
    && docker-php-ext-install -j$(nproc) gd \
    && docker-php-ext-install pdo_mysql \
    && docker-php-ext-install bcmath \
    && docker-php-ext-install zip \
    && rm -rf /var/lib/apt/lists/*


#sockets
#sysvmsg
#xml requires libxml

CMD ["php-fpm"]

EXPOSE 9000
