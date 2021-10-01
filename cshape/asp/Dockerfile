FROM almalinux:latest
USER root

ENV TZ JST-9
ENV TERM xterm

RUN dnf update -y
RUN yum update -y
RUN dnf install vim nodejs npm wget tar git httpd httpd-tools httpd-devel httpd-manual -y

RUN dnf module reset nodejs -y
RUN dnf module install nodejs:14 -y

RUN mkdir /usr/local/src/download
RUN cd /usr/local/src/download

RUN wget https://download.visualstudio.microsoft.com/download/pr/5fcb98bb-21e1-47a5-bb8e-bb25f41a3e52/04811d5d05b7e694f040d2a13c1aae4c/dotnet-sdk-6.0.100-rc.1.21463.6-linux-x64.tar.gz

RUN mkdir /opt/dotnet
RUN tar zxvf dotnet-sdk-6.0.100-rc.1.21463.6-linux-x64.tar.gz -C /opt/dotnet

RUN echo "#!/bin/sh" > /etc/profile.d/dotnet.sh
RUN echo "export DOTNET_ROOT=/opt/dotnet" >> /etc/profile.d/dotnet.sh
RUN echo "export PATH=\$DOTNET_ROOT:\$PATH" >> /etc/profile.d/dotnet.sh
RUN echo "export DOTNET_SYSTEM_GLOBALIZATION_INVARIANT=1" >> /etc/profile.d/dotnet.sh
RUN echo "export ASPNETCORE_ENVIRONMENT=Development" >> /etc/profile.d/dotnet.sh

RUN npm install -g npm-check-updates
RUN npm update