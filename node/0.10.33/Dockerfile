FROM fedora
MAINTAINER JarvisJiang <jarvisjiang@tencent.com>

RUN yum update -y && yum clean all
RUN yum install -y wget gcc gcc-c++ which make
RUN yum clean all

ENV NODE_VERSION 0.10.33

RUN mkdir -p ~/node && cd ~/node \
    && wget http://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.gz \
    && tar -xzvf node-v$NODE_VERSION.tar.gz \
    && cd node-v$NODE_VERSION \
    && ./configure \
    && make && make install

RUN rm -rf ~/node