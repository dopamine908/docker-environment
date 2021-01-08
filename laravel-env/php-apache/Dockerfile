FROM php:8.0.0-apache
EXPOSE 80
EXPOSE 443
RUN apt-get update
RUN apt-get install vim -y
RUN docker-php-ext-install mysqli pdo pdo_mysql
COPY laravel.conf /etc/apache2/sites-available
RUN a2dissite 000-default.conf
RUN a2ensite laravel.conf
RUN a2enmod rewrite
RUN service apache2 restart
