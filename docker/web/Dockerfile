FROM php:7.3-apache

RUN docker-php-ext-install mysqli pdo pdo_mysql
RUN apt-get update -yqq && \
    a2enmod rewrite


COPY default.conf /etc/apache2/sites-enabled/000-default.conf


WORKDIR /var/www/html

CMD ["/usr/sbin/apache2ctl", "-D", "FOREGROUND"]

EXPOSE 80
