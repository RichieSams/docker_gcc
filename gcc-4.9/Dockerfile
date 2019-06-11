FROM ubuntu:xenial

RUN apt-get update \
    # Install pre-reqs
    && apt-get install -y \
        ca-certificates \
        build-essential \
    # Install Tools
        gcc-4.9 \
        g++-4.9 \
        cmake \
    && rm -rf /var/lib/apt/lists/*

RUN rm /usr/bin/gcc && ln /usr/bin/gcc-4.9 /usr/bin/gcc
RUN rm /usr/bin/g++ && ln /usr/bin/g++-4.9 /usr/bin/g++
