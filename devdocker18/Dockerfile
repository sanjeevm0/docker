FROM sanjeevm0/baseimage18
MAINTAINER Sanjeev Mehrotra <sanjeevm@alumni.stanford.edu>     

RUN apt-get install -y --no-install-recommends \
    gpg-agent

# Install docker
RUN curl -q https://get.docker.com/ | bash

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