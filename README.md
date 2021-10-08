# Docker configuration for LEMP Stack


## Install docker

`sudo apt-get install docker.io docker-compose`.

installation documentations [https://docs.docker.com/engine/install]

## Run docker

`docker-compose up -d`


## Set working director in `docker-composer.yml`

```
nginx:
    volumes:
        - WORKING_DIR:/app:consistentc
php
    volumes:
        - WORKING_DIR:/app
```


## App server

`localhost:8000`


## To run phpmyadmin

`localhost:8080`

```
username : root
password : root
```


## Composer install
`sh bin/composer install`



## Mysql
for linux / old mac 
```
image: "mysql:5.7" 
```

for new Mac with M1 chip
```
image: mysql:5.7@sha256:b3b2703de646600b008cbb2de36b70b21e51e7e93a7fca450d2b08151658b2dd
```


## Run `php artisan` commands
`sh bin/artisan $$`


## Import db dump
docker exec -i `docker_mysql_1` mysql -uroot -proot `DATABASE_NAME` < `FILE_NAME.sql`


## Find IP of container
docker inspect -f '{{range .NetworkSettings.Networks}}{{.IPAddress}}{{end}}' `docker_mysql_1`


## If you want to use mondodb
`docker run --name mongodb -p 27017:27017 -d mongo`