FROM php:7.0.11-alpine

MAINTAINER herloct <herloct@gmail.com>

RUN apk update --no-cache && \
    apk add --no-cache su-exec && \
    rm -rf /var/cache/apk/* /var/tmp/* /tmp/*

RUN curl -L https://squizlabs.github.io/PHP_CodeSniffer/phpcbf.phar > /usr/local/bin/phpcbf && \
    chmod +x /usr/local/bin/phpcbf

COPY entrypoint.sh /usr/local/bin/entrypoint.sh

ENTRYPOINT ["entrypoint.sh", "phpcbf"]
CMD ["--version"]
