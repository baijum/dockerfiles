FROM ubuntu:14.04
MAINTAINER Baiju Muthukadan <baiju.m.mail@gmail.com>

RUN echo "deb http://ppa.launchpad.net/saltstack/salt/ubuntu trusty main" > /etc/apt/sources.list.d/saltstack.list
ADD http://keyserver.ubuntu.com:11371/pks/lookup?op=get&search=0x4759FA960E27C0A6 /tmp/salt-ppa.key
RUN apt-key add /tmp/salt-ppa.key
RUN DEBIAN_FRONTEND=noninteractive apt-get update -y

RUN DEBIAN_FRONTEND=noninteractive apt-get install -y -qq salt-master

EXPOSE 4505 4506

VOLUME ["/srv"]

ENTRYPOINT ["/usr/bin/salt-master"]

CMD ["--help"]
