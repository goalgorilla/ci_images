ARG VERSION=latest

FROM solr:$VERSION

ADD config /solr-conf/conf

ENTRYPOINT ["solr-precreate", "drupal", "/solr-conf"]
