FROM ubuntu:14.04
MAINTAINER Baiju Muthukadan <baiju.m.mail@gmail.com>

RUN DEBIAN_FRONTEND=noninteractive apt-get install -y -qq python-zodb

RUN mkdir /var/zeo

EXPOSE 8600 8601

ENTRYPOINT ["/usr/bin/runzeo"]

CMD ["-help"]
