FROM alpine:latest as builder
ARG NRJMX_VERSION
WORKDIR /
ADD http://download.newrelic.com/infrastructure_agent/binaries/linux/noarch/nrjmx_linux_${NRJMX_VERSION}_noarch.tar.gz ./
RUN tar -xzf nrjmx_linux_${NRJMX_VERSION}_noarch.tar.gz

FROM newrelic/infrastructure:latest

ADD integrations.d/nri-config.yml /etc/newrelic-infra/integrations.d

