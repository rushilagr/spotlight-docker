FROM java:openjdk-8-jre

MAINTAINER  DBpedia Spotlight Team <dbp-spotlight-developers@lists.sourceforge.net>

ENV RELEASE_SERVER    downloads.dbpedia-spotlight.org
ENV RELEASE_FILENAME   dbpedia-spotlight-0.8-beta.jar
ENV LANGUAGE_MODEL    it.tar.gz

RUN mkdir -p /opt/spotlight && \
    cd /opt/spotlight && \
    curl -O "http://$RELEASE_SERVER/spotlight/$RELEASE_FILENAME" && \
    curl -O "http://$RELEASE_SERVER/it/demo/$LANGUAGE_MODEL" && \
    tar xvf $LANGUAGE_MODEL  && \
    rm  $LANGUAGE_MODEL


ADD spotlight.sh /bin/spotlight.sh
RUN chmod +x /bin/spotlight.sh

EXPOSE 80
