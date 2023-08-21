FROM php:8.1-fpm
RUN docker-php-ext-install pdo pdo_mysql


# Install necessary tools
RUN apt-get update && apt-get install -y \
       curl \
       unzip \
       git

# Create /var/www directory
RUN mkdir -p /var/www

# Install Composer
RUN curl -sS https://getcomposer.org/composer-stable.phar -o /usr/local/bin/composer && chmod +x /usr/local/bin/composer

# Debugging: list contents of /usr/local/bin and check Composer version
RUN ls -al /usr/local/bin && composer -v

WORKDIR /var/www/symfony