## Install docker

`sudo apt-get install docker.io docker-compose`

## run docker

`docker-composer up -d`

## set app folder in `docker-composer.yml`

```
nginx:
    volumes:
        - ../[PROJECT_DIR_NAME]:/app:consistentc
php
    volumes:
        - ../[PROJECT_DIR_NAME]:/app
```

## app server

`localhost:8000`

## phpmyadmin

`localhost:8080`

```
username : root
password : manish@yipl
```

## run mondodb

`docker run --name mongodb -p 27017:27017 -d mongo:`

## composer install

sh bin/composer install

## php artisan commands

sh bin/artisan $$
