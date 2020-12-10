FROM php:7.4.11-fpm-alpine3.12

LABEL MAINTAINER="studyforzx@gmail.com"

RUN php -r "copy('https://install.phpcomposer.com/installer', 'composer-setup.php');" \
    && php composer-setup.php \
    && php -r "unlink('composer-setup.php');" \
    && mv composer.phar /usr/local/bin/composer \
    && docker-php-ext-install pdo_mysql \
    && docker-php-ext-install bcmath
