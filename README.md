[![](https://images.microbadger.com/badges/image/herloct/phpcbf.svg)](http://microbadger.com/images/herloct/phpcbf "Get your own image badge on microbadger.com")

## Supported tags and respective `Dockerfile` links

* [`2.7.0`, `latest`](https://github.com/herloct/docker-phpcbf/blob/master/2.7.0/Dockerfile)

## What is PHP_CodeSniffer and phpcbf?

PHP_CodeSniffer tokenizes PHP, JavaScript and CSS files and detects violations of a defined set of coding standards.

PHP_CodeSniffer's `phpcbf` is a script to automatically correct coding standard violations.

> https://github.com/squizlabs/PHP_CodeSniffer

## How to use this image

Basic usage using current user id (uid).

```sh
docker run --rm \
    -e LOCAL_USER_ID=$(id -u) \
    -v /local/path:/project \
    herloct/phpcbf [<options>]
```

For example, to fix `src` directory to follow PSR1 and PSR2 standard.

```sh
docker run --rm \
    -e LOCAL_USER_ID=$(id -u) \
    -v /local/path:/project \
    herloct/phpcbf --no-patch --standard=PSR1,PSR2 src
```
