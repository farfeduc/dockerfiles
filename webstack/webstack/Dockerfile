FROM xataz/nginx:1.9.11
MAINTAINER xataz <https://github.com/xataz>

EXPOSE 80 443
VOLUME ["/www","/sites-enabled","/conf.d"]
ENV NGINX_VER=1.9.11 UID=991 GID=991

RUN apk add --update supervisor php-fpm php-ctype php-json php-curl php-gd php-openssl && rm -rf /tmp/* /var/cache/apk/* && \
addgroup -g ${GID} www-data && adduser -H -s /bin/sh -D -G www-data -u ${UID} www-data &&\
chown -R www-data:www-data /www

ADD nginx.conf /etc/nginx/conf/nginx.conf

ADD php-fpm.conf /etc/php/php-fpm.conf

ADD supervisord.conf /etc/supervisor/supervisord.conf

USER root

RUN mkdir /root/logs

CMD ["/usr/bin/supervisord", "-j", "/root/supervisord.pid", "-c", "/etc/supervisor/supervisord.conf"]