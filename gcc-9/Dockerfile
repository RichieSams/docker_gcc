FROM ubuntu:bionic

# Install repos
RUN apt-get update \
    && apt-get install -y software-properties-common \
    && add-apt-repository -y ppa:ubuntu-toolchain-r/test \
    # Install pre-reqs
    && apt-get update \
    && apt-get install -y \
        ca-certificates \
        build-essential \
    # Install Tools
        gcc-9 \
        g++-9 \
        cmake \
    && rm -rf /var/lib/apt/lists/*

RUN rm /usr/bin/gcc && ln /usr/bin/gcc-9 /usr/bin/gcc
RUN rm /usr/bin/g++ && ln /usr/bin/g++-9 /usr/bin/g++
