FROM herucoro/spring_app:latest
USER root

RUN dnf update -y
RUN yum update -y

RUN dnf install git

WORKDIR /usr/local/src

# will add auto install(/opt/amazon-corretto-11-x64-linux-jdk, ln -s /opt/amazon-corretto-11-x64-linux-jdk /opt/java)
# and add path(~/.java.env(JAVA_HOME etc)), 
# change work directory(/root/src/ -> /usr/local/src/)