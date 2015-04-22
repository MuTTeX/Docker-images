FROM ubuntu:14.04

MAINTAINER MuTTeX "m.mailfox@gmail.com"

RUN sudo apt-key update && sudo apt-get update && sudo apt-get install -y nginx

ENV REFRESHED_AT 2015–04–22

# forward request and error logs to docker log collector
RUN ln -sf /dev/stdout /var/log/nginx/access.log
RUN ln -sf /dev/stderr /var/log/nginx/error.log

VOLUME ["/var/cache/nginx"]

EXPOSE 80 443

CMD ["nginx", "-g", "daemon off;"]

