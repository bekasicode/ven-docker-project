FROM romiafrizal/ven-p:1.5

VOLUME /opt/docker/etc/httpd/ssl
VOLUME /var/www/venus
WORKDIR /var/www/venus

RUN useradd -ms /bin/bash memcached
RUN memcached -u memcached -d -m 64 -l 0.0.0.0 -p 11211

RUN npm install fstream
RUN npm install bootstrap
RUN npm install object.assign

EXPOSE 80
EXPOSE 443
EXPOSE 9000
EXPOSE 11211
EXPOSE 8443