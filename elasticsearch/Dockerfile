FROM docker.elastic.co/elasticsearch/elasticsearch:6.5.0


ENV ES_HOME /opt/elasticsearch
WORKDIR ${ES_HOME}

ENV discovery.type single-node
#ENV ES_HEAP_SIZE 2g
ENV ES_HEAP_SIZE 512m
ENV MAX_OPEN_FILES=65535
ENV MAX_LOCKED_MEMORY=unlimited

VOLUME ${ES_HOME}/es-data

EXPOSE 9200 9300
