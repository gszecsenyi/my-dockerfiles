# Inspired by Guido Schmutz
FROM trivadisbds/base:ubuntu

MAINTAINER Gergely Szecsenyi  <gergely.szecsenyi@trivadis.com>

RUN apt-get update && apt-get install -y unzip wget curl docker jq coreutils

#ENV KAFKA_VERSION="0.10.0.0" SCALA_VERSION="2.11"
EXPOSE 8081
ADD content/download-flink.sh /tmp/download-flink.sh
RUN /tmp/download-flink.sh && tar xfz /tmp/flink-1.1.4-bin-hadoop1-scala_2.10.tgz -C /opt && rm /tmp/flink-1.1.4-bin-hadoop1-scala_2.10.tgz

ADD content/start-flink-standalone.sh /usr/bin/start-flink-standalone.sh

#CMD ["start-kafka.sh"]

