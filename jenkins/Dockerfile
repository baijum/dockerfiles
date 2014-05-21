FROM ubuntu:14.04
MAINTAINER Baiju Muthukadan <baiju.m.mail@gmail.com>

ADD http://pkg.jenkins-ci.org/debian-stable/jenkins-ci.org.key /tmp/jenkins-ci.org.key
RUN apt-key add /tmp/jenkins-ci.org.key
RUN echo "deb http://pkg.jenkins-ci.org/debian-stable binary/" > /etc/apt/sources.list.d/jenkins.list
RUN DEBIAN_FRONTEND=noninteractive apt-get update -y
RUN DEBIAN_FRONTEND=noninteractive apt-get install -y -qq jenkins

EXPOSE 9876 9877

VOLUME ["/var/lib/jenkins"]

ENV JENKINS_HOME /var/lib/jenkins

USER jenkins

ENTRYPOINT ["/usr/bin/java"]

CMD ["-help"]
