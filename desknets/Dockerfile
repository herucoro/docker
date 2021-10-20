FROM centos:latest
USER root

ENV TZ JST-9
ENV TERM xterm

RUN dnf update -y
RUN yum update -y

RUN dnf install httpd gcc-c++ make readline-devel zlib-devel wget ncurses -y
