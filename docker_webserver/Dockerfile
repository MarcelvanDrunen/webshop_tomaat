FROM php:7.3-apache
#Install gitmysql
RUN apt-get update && apt-get install -y git libzip-dev zip
RUN docker-php-ext-install pdo pdo_mysql mysqli zip
RUN a2enmod rewrite
#Install Composer
RUN php -r "copy('https://getcomposer.org/installer', 'composer-setup.php');"
RUN php composer-setup.php --install-dir=. --filename=composer
RUN mv composer /usr/local/bin/


EXPOSE 80