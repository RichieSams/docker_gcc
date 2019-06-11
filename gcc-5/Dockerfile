FROM gcc:5

RUN sed -i '/jessie-updates/d' /etc/apt/sources.list
RUN apt-get update && apt-get install -y \
    cmake \
 && rm -rf /var/lib/apt/lists/*
