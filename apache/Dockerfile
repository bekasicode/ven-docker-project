FROM webdevops/php-apache-dev:ubuntu-14.04

COPY ./bo4.apache.conf /opt/docker/etc/httpd/vhost.conf

VOLUME /opt/docker/etc/httpd/ssl
VOLUME /var/www/venus
WORKDIR /var/www/venus

EXPOSE 80
EXPOSE 443
EXPOSE 9000