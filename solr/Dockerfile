ARG VERSION=latest

FROM solr:$VERSION

ADD config-"${VERSION}" /solr-conf/conf

ENTRYPOINT ["solr-precreate", "drupal", "/solr-conf"]