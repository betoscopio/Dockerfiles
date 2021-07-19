FROM betoscopio/php74alpine-ext:1.0

RUN curl -L -o drush.phar https://github.com/drush-ops/drush/releases/download/8.4.8/drush.phar \
    && chmod +x drush.phar \
    && mv drush.phar /usr/local/bin/drush
