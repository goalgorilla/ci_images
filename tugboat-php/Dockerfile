ARG VERSION=apache

FROM tugboatqa/php:$VERSION

ENV COMPOSER_MEMORY_LIMIT=-1

RUN set -x && apt-get update && \
  apt-get -y install libzip-dev jq ssh libxml2-dev && \
  apt-get clean && \
  docker-php-ext-install zip sockets bcmath soap && \
  docker-php-ext-enable sockets bcmath soap

RUN ln -s /etc/apache2/mods-available/rewrite.load /etc/apache2/mods-enabled/rewrite.load

RUN echo "memory_limit = 512M" >> /usr/local/etc/php/conf.d/my-php.ini

RUN rm -rf $DOCROOT/../html.original $DOCROOT

# GMP library.
RUN apt-get install -y libgmp-dev
RUN ln -s /usr/include/x86_64-linux-gnu/gmp.h /usr/local/include/
RUN docker-php-ext-configure gmp
RUN docker-php-ext-install gmp
