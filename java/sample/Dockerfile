FROM adoptopenjdk/openjdk11:latest
USER root

RUN apt-get update
RUN apt update

ENV TZ JST-9
ENV TERM xterm

RUN mkdir -p /root/src
WORKDIR /root/src