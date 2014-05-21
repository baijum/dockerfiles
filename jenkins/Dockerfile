FROM ubuntu:14.04
MAINTAINER Baiju Muthukadan <baiju.m.mail@gmail.com>

ADD http://pkg.jenkins-ci.org/debian-stable/jenkins-ci.org.key /tmp/jenkins-ci.org.key
RUN apt-key add /tmp/jenkins-ci.org.key
RUN echo "deb http://pkg.jenkins-ci.org/debian-stable binary/" > /etc/apt/sources.list.d/jenkins.list
RUN DEBIAN_FRONTEND=noninteractive apt-get update -y

# Uncomment the following 6 lines to use Oracle Java
# RUN DEBIAN_FRONTEND=noninteractive apt-get install -y -qq software-properties-common
# RUN DEBIAN_FRONTEND=noninteractive apt-get install -y --reinstall ca-certificates
# RUN DEBIAN_FRONTEND=noninteractive add-apt-repository -y ppa:webupd8team/java
# RUN DEBIAN_FRONTEND=noninteractive apt-get update -y
# RUN echo oracle-java8-set-default shared/accepted-oracle-license-v1-1 select true | /usr/bin/debconf-set-selections
# RUN DEBIAN_FRONTEND=noninteractive apt-get install -y -qq oracle-java8-set-default

RUN DEBIAN_FRONTEND=noninteractive apt-get install -y -qq jenkins

EXPOSE 9876 9877

VOLUME ["/var/lib/jenkins"]

ENV JENKINS_HOME /var/lib/jenkins

ENTRYPOINT ["/usr/bin/java"]

CMD ["-help"]
