# Base docker image. References:
#   - https://hub.docker.com/_/php
#   - https://github.com/docker-library/docs/blob/master/php/README.md#supported-tags-and-respective-dockerfile-links

# PHP 7.4.5 with FPM under debian buster-slim
FROM php:7.4.5-fpm

# There is no php.ini file defined. This line will select php.ini-development as the official php.ini file
# The path to php.ini directory must be the one declared in PHP info: php -i | grep php.ini
RUN cp $PHP_INI_DIR/php.ini-development $PHP_INI_DIR/php.ini

# Install and enable XDebug
RUN pecl install xdebug && docker-php-ext-enable xdebug

# Need to update repo packages list to use apt-get
RUN apt-get update

# Install Git so composer can fetch packages from GitHub
RUN apt-get install -y git-core

# Install zip utilities so packages downloaded by composer can be decompressed
RUN apt-get install -y unzip

# Install Composer
RUN curl -sS https://getcomposer.org/installer | php -- --install-dir=/usr/local/bin --filename=composer

# Install wget to be able to dowload Symfony CLI
RUN apt-get install -y wget

# Install Symfony CLI
RUN wget https://get.symfony.com/cli/installer -O - | bash &&  mv /root/.symfony/bin/symfony /usr/local/bin/symfony

# Install ICU to be able to install PHP intl
RUN apt-get install -y libicu-dev

# Symfony suggest to "Install and enable the intl extension (used for validators)"
RUN docker-php-ext-install intl

# Symfony suggest to "Install and/or enable a PHP accelerator (highly recommended)"
RUN docker-php-ext-install opcache && docker-php-ext-enable opcache

