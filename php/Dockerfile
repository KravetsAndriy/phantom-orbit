FROM php:7.1-fpm

RUN apt-get update && \
	apt-get install -y libpq-dev libxml2-dev libpng-dev

RUN docker-php-ext-install 	xml opcache gd session mbstring mysqli pdo pdo_mysql pcntl json
RUN docker-php-ext-enable 	xml opcache gd session mbstring mysqli pdo pdo_mysql pcntl json

RUN apt-get install -y libmcrypt-dev libxslt-dev zlib1g-dev libicu-dev g++
RUN docker-php-ext-install mcrypt xsl intl zip

RUN docker-php-ext-install bcmath soap 

EXPOSE 9000
CMD ["php-fpm"]