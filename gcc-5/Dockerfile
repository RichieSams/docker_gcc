FROM gcc:5

RUN sed -i '/jessie-updates/d' /etc/apt/sources.list
RUN deb http://ftp.debian.org/debian jessie-backports main \
  && apt-get update && apt-get -t jessie-backports install -y --no-install-recommends \
         cmake \
  && apt-get clean \
  && rm -rf /var/lib/apt/lists/*
