# Dockerized Redis
Built using Oficial images:
* [PHP](https://hub.docker.com/_/mysql/) altered to install `docker-php-ext-install pdo pdo_mysql mysqli` (check `/php` folder).
* [MySQL](https://hub.docker.com/_/php/).
* [PHPMyAdmin](https://hub.docker.com/r/phpmyadmin/phpmyadmin/).

## Redis Config & Data persistance

Volumes for persistance:
* Find config at `redis/config`
* Sync at `redis/data`

## Build steps
* Change `.env-demo` to `.env` and set values.
```bash
# APP Name
APP=appname

# mysql
MYSQL_HOST=mysql
MYSQL_ROOT_PASSWORD=pwd
MYSQL_DATABASE=db
MYSQL_USER=user
MYSQL_PASSWORD=secret
```

* Run `docker-compose up` (needs [Docker Compose](https://docs.docker.com/compose/) installed).

## Once running
* Go to your [http://localhost/](http://localhost/) and start configurate WordPress.
* PhpMyAdmin at [http://localhost:8080/](http://localhost:8080/).

## Requirements
* [Docker Engine](https://docs.docker.com/installation/).
* [Docker Compose](https://docs.docker.com/compose/).
* [Docker Machine](https://docs.docker.com/machine/) (Mac and Windows only).