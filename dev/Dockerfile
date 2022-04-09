FROM ubuntu:bionic


RUN apt-get update \
    && apt-get upgrade -y \
    && apt-get install make python3.7 python3-pip git -y \
    && rm -rf /var/lib/apt/lists/*

ENTRYPOINT [ "/bin/sh" ]
