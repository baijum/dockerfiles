FROM ubuntu:14.04
MAINTAINER Baiju Muthukadan <baiju.m.mail@gmail.com>

RUN DEBIAN_FRONTEND=noninteractive apt-get install -y -qq memcached

RUN mkdir /var/memcached

EXPOSE 11211

USER daemon

ENTRYPOINT ["/usr/bin/memcached"]

CMD ["-h"]
