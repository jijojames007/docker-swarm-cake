FROM phpdockerio/php80-fpm:latest
WORKDIR /var/www/myapp
COPY cakephp .
# Install selected extensions and other stuff
RUN apt-get update \
    && apt-get -y --no-install-recommends install  php8.0-mysql php8.0-intl php8.0-mbstring php8.0-sqlite3\
    && curl -sL https://deb.nodesource.com/setup_12.x -o /tmp/nodesource_setup.sh\
    && /bin/bash /tmp/nodesource_setup.sh\
    && apt-get -y install nodejs\
    && apt-get clean; rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* /usr/share/doc/*
RUN chown -R www-data: /var/www/myapp
COPY php-ini-overrides.ini /etc/php/8.0/fpm/conf.d/
