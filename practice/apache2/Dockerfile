FROM debian:latest

RUN apt update \
  && apt install -y apache2 php libapache2-mod-php \
  && a2enmod php8.2 \
  && apt clean

COPY ./index.php /var/www/html/

CMD ["apachectl", "-D", "FOREGROUND"]
