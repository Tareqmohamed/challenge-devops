# API/Dockerfile
FROM php:8.1-fpm

# Install Composer globally and php extensions
RUN php -r "copy('https://getcomposer.org/installer', 'composer-setup.php');" \
    && php composer-setup.php --install-dir=/usr/local/bin --filename=composer \
    && php -r "unlink('composer-setup.php');" \
    && docker-php-ext-install mysqli pdo_mysql

# Copy php.ini file
RUN mv "$PHP_INI_DIR/php.ini-production" "$PHP_INI_DIR/php.ini"

WORKDIR /var/www/html

COPY . /var/www/html/