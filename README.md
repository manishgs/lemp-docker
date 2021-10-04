# Docker configuration for LEMP Stack


## Install docker

`sudo apt-get install docker.io docker-compose`.

## Run docker

`docker-composer up -d`

## Set app folder in `docker-composer.yml`

```
nginx:
    volumes:
        - ../[PROJECT_DIR_NAME]:/app:consistentc
php
    volumes:
        - ../[PROJECT_DIR_NAME]:/app
```

## App server

`localhost:8000`

## To run phpmyadmin

`localhost:8080`

```
username : root
password : root
```

## Run mondodb

`docker run --name mongodb -p 27017:27017 -d mongo:`
