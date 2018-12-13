FROM romiafrizal/ven-p:1.1

VOLUME /opt/docker/etc/httpd/ssl
VOLUME /var/www/venus
WORKDIR /var/www/venus

RUN a2enmod rewrite

RUN service apache2 restart

EXPOSE 80
EXPOSE 443
EXPOSE 9000