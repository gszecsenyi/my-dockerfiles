FROM trivadisbds/base:ubuntu

MAINTAINER Gergely Szecsenyi <gergely.szecsenyi@trivadis.com>

RUN apt-get update && apt-get install -y unzip wget docker 

RUN wget -c https://archive.apache.org/dist/kafka/0.8.0/kafka_2.8.0-0.8.0.tar.gz && tar -xzvf kafka_2.8.0-0.8.0.tar.gz && mv kafka_2.8.0-0.8.0 /opt && ln -s /opt/kafka_2.8.0-0.8.0/ /opt/kafka

RUN echo '#!/bin/bash' > /usr/bin/start-kafka.sh && echo "cd /opt/kafka" >> /usr/bin/start-kafka.sh && echo "bin/zookeeper-server-start.sh config/zookeeper.properties & > ~/output.log" >> /usr/bin/start-kafka.sh && echo "bin/kafka-server-start.sh config/server.properties > ~/output.log" >> /usr/bin/start-kafka.sh && echo "tail -f ~/output.log" >> /usr/bin/start-kafka.sh && chmod +x /usr/bin/start-kafka.sh

ENV KAFKA_HOME /opt/kafka_${SCALA_VERSION}-${KAFKA_VERSION}

CMD ["start-kafka.sh"]
