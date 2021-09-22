FROM centos:latest
USER root

RUN dnf update -y
RUN yum update -y
RUN dnf install wget tar -y

RUN mkdir -p /root/src/download
RUN wget -P /root/src/download https://corretto.aws/downloads/latest/amazon-corretto-11-x64-linux-jdk.tar.gz

WORKDIR /root/src

# will add auto install(/opt/amazon-corretto-11-x64-linux-jdk, ln -s /opt/amazon-corretto-11-x64-linux-jdk /opt/java)
# and add path(~/.java.env(JAVA_HOME etc)), 
# change work directory(/root/src/ -> /usr/local/src/)