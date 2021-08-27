FROM node:14.17.1
USER root

RUN apt-get update
RUN apt-get -y install locales && \
    localedef -f UTF-8 -i ja_JP ja_JP.UTF-8
RUN apt-get install -y vim less

RUN apt update

ENV TZ JST-9
ENV TERM xterm

RUN mkdir -p /root/src

WORKDIR /root/src

RUN npm install -g create-react-app