FROM ubuntu:16.04
MAINTAINER Sanjeev Mehrotra <sanjeevm@alumni.stanford.edu>

RUN apt-get update 
RUN apt-get install -y --no-install-recommends \
        apt-utils \
        software-properties-common \
        git \
        curl \
        wget \
        cpio \
        mkisofs \
        apt-transport-https \
        openssh-client \
        ca-certificates \
        sshpass \
        ssh \
        build-essential \
        iputils-ping \
        dnsutils \
        net-tools

# replace python 3.5 with 3.6
RUN apt-get install -y --no-install-recommends \
    python-software-properties

RUN add-apt-repository ppa:jonathonf/python-3.6
RUN apt-get update
RUN apt-get install -y --no-install-recommends python3.6

RUN apt-get install -y --no-install-recommends \
    python3-pip \
    python3-yaml \
    python3-jinja2 \
    python3-setuptools \
    python3-pycurl

RUN wget https://repo.anaconda.com/archive/Anaconda3-5.2.0-Linux-x86_64.sh
RUN bash Anaconda3-5.2.0-Linux-x86_64.sh -b -p /usr/local/anaconda
RUN rm Anaconda3-5.2.0-Linux-x86_64.sh

RUN update-ca-certificates

ENV PATH="${PATH}:/usr/local/anaconda/bin"