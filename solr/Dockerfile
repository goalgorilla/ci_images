ARG VERSION=latest
ARG CONFIG_VERSION=9

FROM solr:$VERSION

ADD config-"${CONFIG_VERSION}" /solr-conf/conf

ENTRYPOINT ["solr-precreate", "drupal", "/solr-conf"]