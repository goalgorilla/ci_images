ARG VERSION=latest@sha256:89cea2ef48e51615503f1b0771a76eb70af24861d5d6ecdfaeee0b4419a5890a
ARG CONFIG_VERSION=9

FROM tugboatqa/solr:$VERSION
#RUN mkdir -p /var/solr/data /var/solr/logs; \
#  (cd /opt/solr/server/solr; cp solr.xml zoo.cfg /var/solr/data/); \
#  cp /opt/solr/server/resources/log4j2.xml /var/solr/log4j2.xml; \
#  find /var/solr -type d -print0 | xargs -0 chmod 0770; \
#  find /var/solr -type f -print0 | xargs -0 chmod 0660;

RUN apt-get update && apt-get upgrade -y && rm -rf /var/lib/apt/lists/*

ARG CONFIG_VERSION

ADD --chown=solr:solr config-"${CONFIG_VERSION}" /solr-conf/conf