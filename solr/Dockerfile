ARG VERSION=latest
ARG CONFIG_VERSION=9

FROM solr:$VERSION
#RUN mkdir -p /var/solr/data /var/solr/logs; \
#  (cd /opt/solr/server/solr; cp solr.xml zoo.cfg /var/solr/data/); \
#  cp /opt/solr/server/resources/log4j2.xml /var/solr/log4j2.xml; \
#  find /var/solr -type d -print0 | xargs -0 chmod 0770; \
#  find /var/solr -type f -print0 | xargs -0 chmod 0660;

ARG CONFIG_VERSION

ADD config-"${CONFIG_VERSION}" /solr-conf/conf

ENTRYPOINT ["docker-entrypoint.sh","solr-precreate", "drupal", "/solr-conf"]