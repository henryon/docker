FROM alpine:3.3

MAINTAINER onkokyo@gmail.com

RUN apk update \
    && apk add squid \
    && apk add curl \
    && rm -rf /var/cache/apk/*

COPY start-squid.sh /usr/local/bin/
COPY squid.conf /etc/squid/squid.conf

ENTRYPOINT ["/usr/local/bin/start-squid.sh"]
