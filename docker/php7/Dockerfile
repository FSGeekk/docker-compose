FROM php:7-fpm-alpine
ENV PATH /path/to/bin/folder:$PATH

RUN  curl -sS https://getcomposer.org/installer | php -- --install-dir=/usr/local/bin —-filename=composer &&  mv /usr/local/bin/composer.phar /usr/local/bin/composer

WORKDIR /var/www/symfony

EXPOSE 9000