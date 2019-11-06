FROM debian:stretch
ENV DEBIAN_FRONTEND noninteractive

RUN apt-get update && \
    apt-get install -y --no-install-recommends locales && \
    rm -rf /var/lib/apt/lists/*

RUN echo "Europe/Budapest" > /etc/timezone && dpkg-reconfigure -f noninteractive tzdata

ADD common/locale.gen /etc/locale.gen
RUN locale-gen && locale -a
ENV LC_CTYPE en_US.UTF-8
