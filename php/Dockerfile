FROM php:5.6-fpm
RUN apt-get update
RUN apt-get install -y libpq-dev 
RUN docker-php-ext-configure pgsql -with-pgsql=/usr/local/pgsql 
RUN docker-php-ext-install pdo pdo_pgsql pgsql 
RUN apt-get install -y libpq-dev libxslt-dev 
RUN docker-php-ext-install xsl
