FROM ghcr.io/taffish-org/debian:12

LABEL maintainer="taffish@163.com"

WORKDIR /root

RUN apt-get update && apt-get install -y curl gcc g++ make hisat2

ENV TAFFISH_ENV=TAFFISH
ENV TAFFISH_NAME=hisat2
