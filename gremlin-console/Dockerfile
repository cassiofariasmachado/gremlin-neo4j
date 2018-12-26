FROM tinkerpop/gremlin-console:3.3.4

ARG GREMLIN_VERSION=3.3.4

COPY ./conf/* /opt/gremlin-console/conf/

COPY ./grapeConfig.xml /root/.groovy/grapeConfig.xml
COPY ./install-neo4j-gremlin.groovy /opt/gremlin-console/install-neo4j-gremlin.groovy

RUN /bin/bash -c "/opt/gremlin-console/bin/gremlin.sh -e install-neo4j-gremlin.groovy"