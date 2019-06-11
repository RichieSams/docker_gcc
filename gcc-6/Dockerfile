FROM ubuntu:bionic

RUN apt-get update \
    # Install pre-reqs
    && apt-get install -y \
        ca-certificates \
        build-essential \
    # Install Tools
        gcc-6 \
        g++-6 \
        cmake \
    && rm -rf /var/lib/apt/lists/*

RUN rm /usr/bin/gcc && ln /usr/bin/gcc-6 /usr/bin/gcc
RUN rm /usr/bin/g++ && ln /usr/bin/g++-6 /usr/bin/g++
