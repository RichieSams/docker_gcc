FROM quay.io/richiesams/ubuntu:xenial

RUN apt-get update \
    # Install pre-reqs
    && apt-get install -y \
        ca-certificates \
        build-essential \
    # Install Tools
        gcc-4.9 \
        g++-4.9 \
    && rm -rf /var/lib/apt/lists/*

RUN rm /usr/bin/gcc && ln /usr/bin/gcc-4.9 /usr/bin/gcc
RUN rm /usr/bin/g++ && ln /usr/bin/g++-4.9 /usr/bin/g++

ADD https://github.com/Kitware/CMake/releases/download/v3.25.2/cmake-3.25.2-Linux-x86_64.sh /cmake-3.25.2-Linux-x86_64.sh
RUN mkdir /opt/cmake \
    && sh /cmake-3.25.2-Linux-x86_64.sh --prefix=/opt/cmake --skip-license \
    && ln -s /opt/cmake/bin/cmake /usr/local/bin/cmake \
    && rm /cmake-3.25.2-Linux-x86_64.sh
