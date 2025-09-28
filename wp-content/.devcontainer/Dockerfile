FROM wordpress:6.4-php8.1-apache

RUN apt-get update \
 && apt-get install -y less git unzip curl mariadb-client \
 && rm -rf /var/lib/apt/lists/*

# install WP-CLI
RUN curl -fsSL -o /usr/local/bin/wp https://raw.githubusercontent.com/wp-cli/builds/gh-pages/phar/wp-cli.phar \
 && chmod +x /usr/local/bin/wp

WORKDIR /var/www/html
RUN chown -R www-data:www-data /var/www/html
