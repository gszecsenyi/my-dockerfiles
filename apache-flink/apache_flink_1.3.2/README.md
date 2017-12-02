# Instructions

Build image:
docker build --tag=gszecsenyi/flink:1.3.2 .

Create container:
docker run -i --name flink_132 -p 8081:8081 -t gszecsenyi/flink:1.3.2 /bin/bash

