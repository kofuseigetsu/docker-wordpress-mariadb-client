# WordPress Docker image with MariaDB Client

This is the WordPress image with MariaDB Client installed.

## How to use this image

```
docker run -d --rm --name wordpress-mariadb-client -p 9000:9000 -e WORDPRESS_DB_HOST=db:3306 -e WORDPRESS_DB_USER=wordpress -e WORDPRESS_DB_PASSWORD=wordpress -e WORDPRESS_TABLE_PREFIX=wp_ -e MYSQL_ROOT_PASSWORD=somewordpress seigetsu/wordpress-mariadb-client:5.4.2-php7.4-fpm-alpine
```

## Tags

- `:<baseimage-tag>` : latest version of this image based on the image of `wordpress:<baseimage-tag>`.
- `:<baseimage-tag>-<version>` : Specific version of this image based on the image of `wordpress:<baseimage-tag>`.

## Environment Variables

- `WORDPRESS_DB_HOST` : Host name of WordPress database.
- `WORDPRESS_DB_USER` : User name of WordPress database.
- `WORDPRESS_DB_PASSWORD` : User password of WordPress database.
- `WORDPRESS_TABLE_PREFIX` : Table prefix of WordPress database.
- `MYSQL_ROOT_PASSWORD` : Password for mysql root user.

## Relationship between Source code and Docker image tag

- `<baseimage-tag>` : see directory.
- `<version>` : see branch.

Example:

`seigetsu/wordpress-mariadb-client:5.4.2-php7.4-fpm-alpine-v1.0` :

- branch `v1.0`
- directory `5.4.2-php7.4-fpm-alpine`

## Image Repository

https://hub.docker.com/r/seigetsu/wordpress-mariadb-client

## Automated Build configurations on Docker Hub

- SOURCE REPOSITORY : `kofuseigetsu/docker-wordpress-mariadb-client`
- AUTOTEST : `Off`
- REPOSITORY LINKS : `Off`
- BUILD RULES :  
  | Source Type | Source | Docker Tag | Dockerfile location | Build Context | Autobuild | Build Caching |
  | -------| -------------- | ---------------------------- | ---------- | ------------------------ | --- | --- |
  | Branch | main           | 5.4.2-php7.4-fpm-alpine      | Dockerfile | /5.4.2-php7.4-fpm-alpine | Yes | No  |
  | Branch | /^(v[0-9.]+)$/ | 5.4.2-php7.4-fpm-alpine-{\1} | Dockerfile | /5.4.2-php7.4-fpm-alpine | Yes | No  |
