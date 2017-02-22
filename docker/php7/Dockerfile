FROM php:7-fpm-alpine
ENV PATH /path/to/bin/folder:$PATH



RUN docker-php-ext-install \
    opcache \
    pdo \
    pdo_mysql \
    mysqli


RUN pecl install apcu apc xcache eacceerator

ADD symfony.ini /etc/php5/fpm/conf.d/
ADD symfony.ini /etc/php5/cli/conf.d/

RUN curl -sS https://getcomposer.org/installer | php -- --install-dir=/usr/local/bin —-filename=composer &&  mv /usr/local/bin/composer.phar /usr/local/bin/composer

WORKDIR /var/www/symfony

EXPOSE 9000
