FROM ubuntu:18.04
RUN apt-get update &&           \
    apt-get -y install curl &&     \
    rm -rf /var/lib/apt/lists/*
COPY start.sh /root/
CMD sh /root/start.sh
