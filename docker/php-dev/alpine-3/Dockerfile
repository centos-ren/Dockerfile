#+++++++++++++++++++++++++++++++++++++++
# Dockerfile for webdevops/php-dev:alpine-3
#    -- automatically generated  --
#+++++++++++++++++++++++++++++++++++++++

FROM webdevops/php:alpine-3

MAINTAINER info@webdevops.io
LABEL vendor=WebDevOps.io
LABEL io.webdevops.layout=8
LABEL io.webdevops.version=0.57.1

COPY conf/ /opt/docker/

# Install development environment
RUN /usr/local/bin/apk-install \
        # Install tools
        graphviz \
        # Install php development stuff
        php5-xdebug \
    && /opt/docker/bin/provision run --tag bootstrap --role webdevops-php-dev \
    && /opt/docker/bin/bootstrap.sh

