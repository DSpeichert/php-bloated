# Docker image for PHP-FPM with too many useful extensions

![](https://github.com/DSpeichert/php-bloated/workflows/docker%20build%20PHP%207.4/badge.svg)

Ideally, when creating a Docker image for your application, you'd custom-tailor the Dockerfile
to include only the extensions you need. I found myself doing that a lot. It takes time and
at a scale of many containers per host, makes it impossible to reuse the image, because it's not
essentially shared among containers. It also takes almost **half an hour to build** such an image.

Universal PHP-FPM Docker image with almost everything you might need to run typical and more
exotic PHP apps. It's commonly used by me for Laravel apps.

It's a great idea to use this image instead of: `FROM php:7.4-fpm`.

Use as: `FROM docker.pkg.github.com/dspeichert/php-bloated/php-7.4:latest`.

More versions might be available in future.

Check out the [amazing tool](https://github.com/mlocati/docker-php-extension-installer)
that makes it possible to build an image with so many different PHP extensions so easily.
