ARG VERSION=latest

FROM tugboatqa/solr:$VERSION

ADD config /solr-conf/conf

ENTRYPOINT ["solr-precreate", "drupal", "/solr-conf"]
