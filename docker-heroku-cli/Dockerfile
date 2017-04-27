# See:
# https://devcenter.heroku.com/articles/heroku-cli#debian-ubuntu

FROM debian:jessie

ENV DEBIAN_FRONTEND noninteractive

RUN \
    apt-get update && \
    apt-get dist-upgrade --yes && \
    apt-get install --yes --force-yes --no-install-recommends \
        apt-transport-https \
        curl \
        software-properties-common && \
    apt-get clean

RUN apt-get install software-properties-common # debian only
RUN add-apt-repository "deb https://cli-assets.heroku.com/branches/stable/apt ./"
RUN curl -L https://cli-assets.heroku.com/apt/release.key | apt-key add -
RUN apt-get update
RUN apt-get install --yes --force-yes --no-install-recommends heroku
