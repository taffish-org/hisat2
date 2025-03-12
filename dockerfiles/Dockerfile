FROM ghcr.io/taffish-org/python:3.12.9

LABEL maintainer="taffish@163.com"

WORKDIR /root

RUN apt-get update && apt-get install -y curl gcc g++ make

RUN curl -LO https://github.com/DaehwanKimLab/hisat2/archive/refs/tags/v2.2.1.tar.gz && \
    tar -zxvf /root/v2.2.1.tar.gz && cd /root/hisat2-2.2.1/ && \
    sed -i 's/-m32//g; s/-msse2//g' Makefile && \
    make && cp hisat2 /usr/local/bin/ && \
    for i in $(ls | grep "^hisat2" | grep -v "\.cpp$" | grep "hisat2[-_]") ; do cp $i /usr/local/bin/ ; done

ENV TAFFISH_ENV=TAFFISH
ENV TAFFISH_NAME=hisat2
