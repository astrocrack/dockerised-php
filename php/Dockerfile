FROM php:5.6-fpm

RUN apt-get update
# Install Postgre PDO
RUN echo -e “$(hostname -i)\t$(hostname) $(hostname).localhost” >> /etc/hosts
RUN apt-get install -y libpq-dev libxslt-dev sendmail libc-client-dev libkrb5-dev\
    && docker-php-ext-configure pgsql -with-pgsql=/usr/local/pgsql \
    && docker-php-ext-install xsl pdo pdo_pgsql pgsql gettext 
RUN docker-php-ext-configure imap --with-kerberos --with-imap-ssl
RUN docker-php-ext-install imap