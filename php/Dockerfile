FROM php:8-fpm

RUN chmod 1777 /tmp

RUN docker-php-ext-install mysqli

COPY ./php.ini-production $PHP_INI_DIR/php.ini

RUN apt-get update && apt-get install -y cron procps supervisor

COPY crontab /etc/cron.d/my-crontab

RUN touch /var/log/cron.log

RUN chmod 0644 /etc/cron.d/my-crontab && crontab /etc/cron.d/my-crontab

COPY supervisord.conf /etc/supervisor/supervisord.conf

CMD ["/usr/bin/supervisord"]
