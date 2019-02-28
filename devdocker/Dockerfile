FROM ubuntu:16.04
MAINTAINER Sanjeev Mehrotra <sanjeevm@alumni.stanford.edu>

RUN apt-get update 
RUN apt-get install -y --no-install-recommends \
        apt-utils \
        software-properties-common \
        git \
        curl \
        python-pip \
        wget \
        cpio \
        mkisofs \
        apt-transport-https \
        openssh-client \
        ca-certificates \
        sshpass \
        python-yaml \
        python-jinja2 \
        python-setuptools \
        python-tzlocal \
        iputils-ping \
        dnsutils \
        python-pycurl        

# Install docker
RUN curl -q https://get.docker.com/ | bash

# Install go pre-reqs
RUN apt-get update && apt-get install -y --no-install-recommends \
        ssh \
        mercurial \
        build-essential \
        net-tools

RUN update-ca-certificates

# Install Go
ENV GOVERSION=1.11
ENV GOOS=linux
ENV GOARCH=amd64
RUN wget https://storage.googleapis.com/golang/go$GOVERSION.$GOOS-$GOARCH.tar.gz
RUN echo go$GOVERSION.$GOOS-$GOARCH.tar.gz
RUN tar -C /usr/local -xzf go$GOVERSION.$GOOS-$GOARCH.tar.gz
RUN rm go$GOVERSION.$GOOS-$GOARCH.tar.gz
ENV PATH=$PATH:/usr/local/go/bin

ENV GOPATH=/go

