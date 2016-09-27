[Docker](http://www.docker.com/) image for [PHP_CodeSniffer](http://php.net)'s `phpcbf`.

[![](https://images.microbadger.com/badges/image/herloct/phpcbf.svg)](http://microbadger.com/images/herloct/phpcbf "Get your own image badge on microbadger.com") [![](https://images.microbadger.com/badges/version/herloct/phpcbf.svg)](http://microbadger.com/images/herloct/phpcbf "Get your own version badge on microbadger.com")

## What's Inside

This image is based on [official PHP 7.0 image](https://hub.docker.com/_/php/),
using Alpine Linux instead of Debian for smaller size.

## Supported tags and respective `Dockerfile` links

* [`2.7.0`, `latest`](https://github.com/herloct/docker-phpcbf/blob/master/2.7.0/Dockerfile)

## How to use this image

Basic usage using current user id (uid).

```sh
docker run --rm \
    -e LOCAL_USER_ID=$(id -u) \
    -v /local/path:/project \
    -w /project \
    herloct/phpcbf [<options>]
```

For example, to fix `src` directory to PSR1 and PSR2 standard.

```sh
docker run --rm \
    -e LOCAL_USER_ID=$(id -u) \
    -v /local/path:/project \
    -w /project \
    herloct/phpcbf --no-patch --standard=PSR1,PSR2 src
```
