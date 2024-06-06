# Dockerfile-web
FROM php:7.4-apache

# Install necessary PHP extensions
RUN apt-get update && apt-get install -y libpng-dev libjpeg-dev libfreetype6-dev \
    && docker-php-ext-configure gd --with-freetype --with-jpeg \
    && docker-php-ext-install gd pdo pdo_mysql mysqli

COPY src/ /var/www/html/

EXPOSE 80
