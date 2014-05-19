FROM ubuntu:14.04
MAINTAINER Baiju Muthukadan <baiju.m.mail@gmail.com>

RUN apt-get install -y -qq unzip

RUN mkdir /var/consul
RUN mkdir /usr/local/share/consul

ADD https://dl.bintray.com/mitchellh/consul/0.2.0_linux_amd64.zip /tmp/consul.zip
RUN unzip /tmp/consul.zip -d /usr/local/bin
RUN chmod +x /usr/local/bin/consul

ADD https://dl.bintray.com/mitchellh/consul/0.2.0_web_ui.zip /tmp/consul_web_ui.zip
RUN unzip /tmp/consul_web_ui.zip -d /usr/local/share/consul

EXPOSE 8400 8500 8600/udp 8301 8302

ENTRYPOINT ["/usr/local/bin/consul", "agent"]

CMD ["-help"]
