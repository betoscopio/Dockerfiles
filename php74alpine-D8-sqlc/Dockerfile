FROM betoscopio/php74alpine-d8:1.0

RUN apk update \
    && apk add --update-cache --no-cache mariadb-client \
    && rm -rf /var/cache/apk/*
