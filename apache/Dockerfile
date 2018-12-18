FROM romiafrizal/ven-p:1.3

VOLUME /opt/docker/etc/httpd/ssl
VOLUME /var/www/venus
WORKDIR /var/www/venus

RUN apt-get install -y memcached

RUN echo '[Memcache]' >> /opt/docker/etc/php/php.ini
RUN echo 'memcache.allow_failover = 1' >> /opt/docker/etc/php/php.ini
RUN echo 'memcache.max_failover_attempts = 20' >> /opt/docker/etc/php/php.ini
RUN echo 'memcache.chunk_size = 8192' >> /opt/docker/etc/php/php.ini
RUN echo 'memcache.default_port = 11211' >> /opt/docker/etc/php/php.ini


EXPOSE 80
EXPOSE 443
EXPOSE 9000