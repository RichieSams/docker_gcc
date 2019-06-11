FROM ubuntu:bionic

RUN apt-get update \
    # Install pre-reqs
    && apt-get install -y \
        ca-certificates \
        build-essential \
    # Install Tools
        gcc-8 \
        g++-8 \
        cmake \
    && rm -rf /var/lib/apt/lists/*

RUN rm /usr/bin/gcc && ln /usr/bin/gcc-8 /usr/bin/gcc
RUN rm /usr/bin/g++ && ln /usr/bin/g++-8 /usr/bin/g++
