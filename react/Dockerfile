FROM almalinux:latest
USER root

RUN dnf update -y
RUN yum update -y
RUN dnf install -y vim nodejs npm httpd httpd-tools httpd-devel httpd-manual git
RUN dnf module reset nodejs -y
RUN dnf module install nodejs:14 -y

ENV TZ JST-9
ENV TERM xterm

RUN mkdir -p /root/src
RUN mkdir -p /root/src/download

WORKDIR /root/src

RUN npm install -g create-react-app