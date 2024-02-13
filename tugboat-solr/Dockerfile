ARG VERSION=latest
ARG CONFIG_VERSION=9

FROM tugboatqa/solr:$VERSION

ADD --chown=solr:solr config-"${CONFIG_VERSION}" /solr-conf/conf