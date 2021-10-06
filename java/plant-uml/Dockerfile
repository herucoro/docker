FROM almalinux:latest
USER root

RUN dnf update -y
RUN yum update -y
RUN dnf install wget tar git -y

RUN mkdir /usr/local/src/download
RUN cd /usr/local/src/download

RUN wget https://corretto.aws/downloads/latest/amazon-corretto-11-x64-linux-jdk.tar.gz 
RUN tar zxvf amazon-corretto-11-x64-linux-jdk.tar.gz -C /opt/

RUN ln -s /opt/amazon-corretto-11.0.12.7.1-linux-x64 /opt/java

RUN echo "#!/bin/sh" > /etc/profile.d/java.sh
RUN echo "export JAVA_HOME=/opt/java" >> /etc/profile.d/java.sh
RUN echo "export PATH=\$JAVA_HOME/bin:\$PATH" >> /etc/profile.d/java.sh
RUN echo "export CLASSPATH=." >> /etc/profile.d/java.sh

RUN dnf install graphviz -y

# "Ctrl + P" と入力して、Quick Open を開く
# Quick Open に ext install plantuml と入力して、Enter キーを押す

WORKDIR /usr/local/src