FROM ubuntu:14.04
MAINTAINER Baiju Muthukadan <baiju.m.mail@gmail.com>

RUN DEBIAN_FRONTEND=noninteractive apt-get install -y -qq mongodb

VOLUME ["/data"]

EXPOSE 27017 28017

ENTRYPOINT ["/usr/bin/mongod"]

CMD ["--help"]
