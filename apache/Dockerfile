FROM romiafrizal/ven-p:1.2

VOLUME /opt/docker/etc/httpd/ssl
VOLUME /var/www/venus
WORKDIR /var/www/venus

RUN a2enmod rewrite
RUN a2enmod remoteip
RUN a2dismod mpm_event
RUN a2dismod mpm_worker

RUN service apache2 restart

RUN a2enmod mpm_prefork

RUN service apache2 restart

RUN apt-get install libssh2-1-dev libssh2-phpc

EXPOSE 80
EXPOSE 443
EXPOSE 9000