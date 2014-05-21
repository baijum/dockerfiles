FROM ubuntu:14.04
MAINTAINER Baiju Muthukadan <baiju.m.mail@gmail.com>

RUN DEBIAN_FRONTEND=noninteractive apt-get install -y -qq software-properties-common
RUN DEBIAN_FRONTEND=noninteractive apt-get install -y --reinstall ca-certificates
RUN DEBIAN_FRONTEND=noninteractive add-apt-repository -y ppa:nginx/stable
RUN DEBIAN_FRONTEND=noninteractive apt-get update -y
RUN DEBIAN_FRONTEND=noninteractive apt-get install -y -qq nginx

RUN echo "\ndaemon off;" >> /etc/nginx/nginx.conf && \
  chown -R www-data:www-data /var/lib/nginx

EXPOSE 80 443

VOLUME ["/data", "/etc/nginx/sites-enabled", "/var/log/nginx"]

WORKDIR /etc/nginx

ENTRYPOINT ["/usr/sbin/nginx"]

CMD ["-h"]
