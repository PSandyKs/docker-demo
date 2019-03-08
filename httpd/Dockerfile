# This image will build apache web server image with code

FROM ubuntu:12.04

MAINTAINER Goutham <example.com>

LABEL AppName="PetClinic" \
      reldate="9-3-2019"

ENV APACHE_RUN_USER www-data
ENV APACHE_RUN_GROUP www-data
ENV APACHE_LOG_DIR /var/log/apache2

EXPOSE 80

COPY index.html /var/www/

# COPY httpd.conf

RUN apt-get update && apt-get install -y apache2

CMD ["/usr/sbin/apache2", "-D", "FOREGROUND"]
