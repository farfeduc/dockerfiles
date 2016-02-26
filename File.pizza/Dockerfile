FROM xataz/alpine:3.3
MAINTAINER xataz <https://github.com/xataz>

EXPOSE 3000

RUN apk add --update nodejs && rm -rf /tmp/* /var/cache/apk/* && npm install filepizza -g

CMD ["filepizza"]