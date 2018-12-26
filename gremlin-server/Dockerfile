FROM tinkerpop/gremlin-server:3.3.4

ARG GREMLIN_VERSION=3.3.4

COPY ./conf/* /conf/

EXPOSE 8182

RUN /bin/bash -c "/opt/gremlin-server/bin/gremlin-server.sh install org.apache.tinkerpop neo4j-gremlin $GREMLIN_VERSION"
