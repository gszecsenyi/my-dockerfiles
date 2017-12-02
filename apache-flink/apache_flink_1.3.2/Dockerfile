# Inspired by Guido Schmutz
FROM trivadisbds/base:ubuntu

MAINTAINER Gergely Szecsenyi  <gergely.szecsenyi@trivadis.com>

RUN apt-get update && apt-get install -y unzip wget curl docker jq coreutils

EXPOSE 8081
RUN wget -c http://tux.rainside.sk/apache/flink/flink-1.3.2/flink-1.3.2-bin-hadoop27-scala_2.11.tgz && tar -xzvf flink-1.3.2-bin-hadoop27-scala_2.11.tgz && mv flink-1.3.2 /opt && ln -s /opt/flink-1.3.2 /opt/flink

ADD content/start-flink-standalone.sh /usr/bin/start-flink-standalone.sh

#CMD ["start-kafka.sh"]

