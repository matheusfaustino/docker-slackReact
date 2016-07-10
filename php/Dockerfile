FROM php:7.0-cli

WORKDIR /var/www

COPY config/php.ini-development /usr/local/etc/php/

RUN apt-get update && apt-get install -y \
    vim \
    git \
    curl \
    zlib1g-dev \
    libmcrypt-dev \
    && docker-php-ext-install -j$(nproc) zip pdo pdo_mysql mbstring opcache sockets

# change php timezone
RUN echo "date.timezone = America/Sao_Paulo" >> /usr/local/etc/php/php.ini

# add composer
RUN curl -sS https://getcomposer.org/installer | php -- --install-dir=/usr/local/bin --filename=composer

# execute composer without Xdebug
RUN echo "alias composer='php -n -dextension=zip.so /usr/local/bin/composer'" >> ~/.bashrc \
    && echo "export TERM=xterm" >> ~/.bashrc

EXPOSE 80
