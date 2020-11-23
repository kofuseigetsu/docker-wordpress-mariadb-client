FROM wordpress:5.4.2-php7.4-fpm-alpine

# install
RUN apk -U add mariadb-client --no-cache

ENTRYPOINT ["docker-entrypoint.sh"]
CMD ["php-fpm"]
