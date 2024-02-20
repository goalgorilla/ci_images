ARG VERSION=latest
ARG CONFIG_VERSION=9

FROM solr:$VERSION

ARG CONFIG_VERSION

ADD config-"${CONFIG_VERSION}" /solr-conf/conf

ENTRYPOINT ["docker-entrypoint.sh", "solr-precreate", "drupal", "/solr-conf"]
