FROM webdevops/php-apache-dev:ubuntu-14.04

COPY ./bo4.apache.conf /opt/docker/etc/httpd/vhost.conf

VOLUME /opt/docker/etc/httpd/ssl
VOLUME /var/www/venus
WORKDIR /var/www/venus

RUN apt-get update
RUN apt-get install -y nodejs
RUN apt-get install -y npm
RUN npm config set strict-ssl false
RUN npm install -g less
RUN npm install -g handlebars
RUN npm install -g uglify-js
RUN npm install -g uglifycss

EXPOSE 80
EXPOSE 443
EXPOSE 9000