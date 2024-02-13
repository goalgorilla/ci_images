ARG VERSION=latest

FROM solr:$VERSION

ARG CONFIG_VERSION

ADD config-"${CONFIG_VERSION}" /solr-conf/conf

ENTRYPOINT ["solr-precreate", "drupal", "/solr-conf"]