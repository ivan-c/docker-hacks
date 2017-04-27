FROM debian:jessie

ENV DEBIAN_FRONTEND noninteractive

RUN \
    apt-get update && \
    apt-get dist-upgrade --yes && \
    apt-get install --yes --force-yes --no-install-recommends \
        ca-certificates && \
    apt-get clean

ADD https://github.com/daticahealth/cli/releases/download/3.4.2/datica_3.4.2_linux_amd64.deb .
RUN dpkg --install *.deb

ENTRYPOINT ["/usr/bin/datica"]
