FROM betoscopio/php81alpine-d9:1.0

RUN apk update \
    && apk add --update-cache --no-cache mariadb-client \
    && rm -rf /var/cache/apk/*
