# Custom Docker Files

Some Dockerfiles for images of my frecuent use:

- [php74debian](https://hub.docker.com/repository/docker/betoscopio/php74-debian-ext): Official PHP 7.4 image based on Debian with some extra modules installed.
- [php74alpine](https://hub.docker.com/repository/docker/betoscopio/php74alpine-ext): Official PHP 7.4 image based on Alpine with some extra modules installed.
- [php74alpine-D7](https://hub.docker.com/repository/docker/betoscopio/php74alpine-d7): Official PHP 7.4 image based on Alpine with some extra modules and Drush 8 installed.
- [php74alpine-D7-sqlc](https://hub.docker.com/repository/docker/betoscopio/php74alpine-d7): Official PHP 7.4 image based on Alpine with some extra modules,Drush 8 and mariadb-client installed.
- [php74alpine-D8](https://hub.docker.com/repository/docker/betoscopio/php74alpine-d8): Official PHP 7.4 image based on Alpine with some extra modules Drush launcher and composer.
- [php74alpine-D8-sqlc](https://hub.docker.com/repository/docker/betoscopio/php74alpine-d8): Official PHP 7.4 image based on Alpine with some extra modules, Drush launcher, composer and mariadb-client installed.
- [php81alpine](https://hub.docker.com/repository/docker/betoscopio/php81alpine-ext): Official PHP 8.1 image based on Alpine with some extra modules installed.
- [php81alpine-D9](https://hub.docker.com/repository/docker/betoscopio/php81alpine-d9): Official PHP 8.1 image based on Alpine with some extra modules Drush launcher and composer.
- [php81alpine-D9-sqlc](https://hub.docker.com/repository/docker/betoscopio/php81alpine-d9): Official PHP 8.1 image based on Alpine with some extra modules, Drush launcher, composer and mariadb-client installed.

Local building:
```
//just build
$ docker build <directory> -t user/image-name:tag

//create tag
$ docker tag image-id username/image-name:tag

//upload image
$ docker login
$ docker push username/image-name:tag
``` 