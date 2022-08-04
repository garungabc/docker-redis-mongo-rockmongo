FROM phpdockerio/php72-fpm:latest
WORKDIR "/application"

# Fix debconf warnings upon build
ARG DEBIAN_FRONTEND=noninteractive

# Install selected extensions and other stuff
RUN apt-get update \
    && apt-get -y --no-install-recommends install php7.2-mongodb php7.2-intl \
    && apt-get -y install iputils-ping wget \
    && apt-get -y install telnet \
    && apt-get -y install nano vim \
    && apt-get -y install redis-server php7.2-dev php7.2-igbinary php7.2-redis \
    && apt-get -y install php7.2-phalcon \
    && apt-get clean; rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* /usr/share/doc/*
