FROM quay.io/richiesams/ubuntu:jammy

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
        gcc-12 \
        g++-12 \
        valgrind \
        xxd \
        glslang-tools \
    && rm -rf /var/lib/apt/lists/*

RUN rm /usr/bin/gcc && ln /usr/bin/gcc-12 /usr/bin/gcc
RUN rm /usr/bin/g++ && ln /usr/bin/g++-12 /usr/bin/g++

ADD https://github.com/Kitware/CMake/releases/download/v3.25.2/cmake-3.25.2-Linux-x86_64.sh /cmake-3.25.2-Linux-x86_64.sh
RUN mkdir /opt/cmake \
    && sh /cmake-3.25.2-Linux-x86_64.sh --prefix=/opt/cmake --skip-license \
    && ln -s /opt/cmake/bin/cmake /usr/local/bin/cmake \
    && rm /cmake-3.25.2-Linux-x86_64.sh
