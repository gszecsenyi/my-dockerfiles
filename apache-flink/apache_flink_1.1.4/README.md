# Instructions

# Instructions

Build image:
docker build --tag=gszecsenyi/flink:1.1.4 .

Create container:
docker run -i --name flink_114 -p 8081:8081 -t gszecsenyi/flink:1.1.4 /bin/bash
