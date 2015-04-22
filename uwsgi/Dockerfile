FROM ubuntu:14.04

MAINTAINER MuTTeX "m.mailfox@gmail.com"

# RUN echo "deb http://archive.ubuntu.com/ubuntu/ $(lsb_release -sc) main universe" >> /etc/apt/sources.list

ENV REFRESHED_AT 2015–04–22

RUN apt-get update

RUN apt-get install -y build-essential python3 python3-dev python3-pip

RUN pip3 install uwsgi

RUN mkdir -p sudo mkdir /etc/uwsgi/vassals

EXPOSE 8080

# run the emperor
CMD ["uwsgi", "--emperor", "/etc/uwsgi/vassals", "--uid", "www-data", "--gid", "www-data"]