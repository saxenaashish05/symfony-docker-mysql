FROM php:8.0-fpm

RUN apt update \
    && apt install -y zlib1g-dev g++ git libicu-dev zip libzip-dev zip \
    && docker-php-ext-install  intl opcache pdo pdo_mysql \
    && pecl install apcu \
    && docker-php-ext-enable apcu \
    && docker-php-ext-configure zip \
    && docker-php-ext-install zip
RUN docker-php-ext-install mysqli
RUN docker-php-ext-enable mysqli
WORKDIR /var/www/html/symfony_docker-mysql

RUN curl -sS https://getcomposer.org/installer | php -- --install-dir=/usr/local/bin --filename=composer

RUN curl -sS https://get.symfony.com/cli/installer | bash

RUN mkdir -p /usr/local/bin


RUN apt-get -y install  wget

# RUN apt-get -y install sudo wget

RUN wget --quiet https://get.symfony.com/cli/installer -O - | bash

#RUN mv /root/.symfony/bin/symfony /usr/local/bin/symfony

RUN git config --global user.email "splendid.saxena@gmail.com" \ 
    && git config --global user.name "Ashish Kumar Saxena"