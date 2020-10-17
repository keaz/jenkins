FROM jenkins/inbound-agent:alpine

LABEL MAINTAINER="Kasun Ranasinghe <kasunranasinghe303@gmail.com>"
LABEL Description="This is a base image, which allows connecting Jenkins agents via JNLP protocols"

USER root
# Alpine seems to come with libcurl baked in, which is prone to mismatching
# with newer versions of curl. The solution is to upgrade libcurl.
RUN apk update && apk add -u libcurl curl
# Install Docker client
ARG DOCKER_VERSION=18.03.0-ce

RUN curl -fsSL https://download.docker.com/linux/static/stable/`uname -m`/docker-$DOCKER_VERSION.tgz | tar --strip-components=1 -xz -C /usr/local/bin docker/docker
RUN touch /debug-flag
#VOLUME /var/run/docker.sock
#RUN chown jenkins:jenkins /var/run/docker.sock

#USER jenkins
