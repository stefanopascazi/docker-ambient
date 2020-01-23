FROM php:latest-fpm

# MYSQLI 
RUN docker-php-ext-install mysqli

# PDO_MYSQLI 
RUN docker-php-ext-install pdo_mysql

RUN touch /usr/local/etc/php/conf.d/uploads.ini \
    && echo "upload_max_filesize=64M;\r\n post_max_size=128M;\r\nmemory_limit = 512M" >> /usr/local/etc/php/conf.d/uploads.ini

EXPOSE 9000
CMD ["php-fpm"]
