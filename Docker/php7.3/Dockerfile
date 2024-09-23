FROM php:7.3-fpm
RUN apt-get update
RUN apt-get upgrade -y
RUN apt-get install libzip-dev -y
RUN apt-get install zip unzip -y
RUN apt-get install git -y
RUN apt-get install curl -y
RUN apt-get install libxml2-dev -y
RUN apt-get install libldap2-dev -y
RUN apt-get install libgd-dev -y

RUN docker-php-ext-install ldap
RUN docker-php-ext-install soap
RUN docker-php-ext-install zip
RUN docker-php-ext-install mysqli
RUN docker-php-ext-install bcmath
RUN docker-php-ext-install ctype
RUN docker-php-ext-install fileinfo
RUN docker-php-ext-install pdo
RUN docker-php-ext-install pdo_mysql
RUN docker-php-ext-install tokenizer

RUN curl -sS https://getcomposer.org/installer | php -- --install-dir=/usr/local/bin --filename=composer
RUN chown -R www-data:www-data /var/www/html