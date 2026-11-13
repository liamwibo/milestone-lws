FROM alpine:latest

RUN apk add lighttpd

COPY ./html /var/www/servers/milestone-web/
COPY ./lighttpd.conf /etc/lighttpd/lighttpd.conf

RUN chown -R lighttpd:lighttpd /var/www/servers/milestone-web/

EXPOSE 80

CMD ["lighttpd", "-D", "-f", "/etc/lighttpd/lighttpd.conf"]