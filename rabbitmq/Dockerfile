FROM ubuntu:14.04
MAINTAINER Baiju Muthukadan <baiju.m.mail@gmail.com>

RUN DEBIAN_FRONTEND=noninteractive apt-get install -y -qq rabbitmq-server
RUN rabbitmq-plugins enable rabbitmq_management

EXPOSE 5672 15672

ENTRYPOINT ["/usr/sbin/rabbitmq-server"]

CMD ["--help"]
