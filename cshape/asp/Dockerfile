FROM ubuntu:latest
USER root

ENV TZ JST-9
ENV TERM xterm

# RUN apt upgrade -y
# RUN apt-get upgrade -y
# RUN apt-get update -y
RUN apt update -y
# RUN apt install vim nodejs npm wget tar git httpd httpd-tools httpd-devel httpd-manual -y
# RUN apt install vim nodejs npm wget tar git apache2 -y
# RUN apt install vim wget tar git apache2 -y
RUN apt install vim wget tar -y

# RUN apt module reset nodejs -y
# RUN apt module install nodejs:14 -y

RUN mkdir /usr/local/src/download
RUN cd /usr/local/src/download

# Download .NET6 SDK
RUN wget https://download.visualstudio.microsoft.com/download/pr/ede8a287-3d61-4988-a356-32ff9129079e/bdb47b6b510ed0c4f0b132f7f4ad9d5a/dotnet-sdk-6.0.101-linux-x64.tar.gz


RUN mkdir /opt/dotnet
RUN tar zxvf dotnet-sdk-6.0.101-linux-x64.tar.gz -C /opt/dotnet

# add dotnet command path
RUN echo "#!/bin/sh" > /etc/profile.d/dotnet.sh
RUN echo "export DOTNET_ROOT=/opt/dotnet" >> /etc/profile.d/dotnet.sh
RUN echo "export PATH=\$DOTNET_ROOT:\$PATH" >> /etc/profile.d/dotnet.sh
RUN echo "export DOTNET_SYSTEM_GLOBALIZATION_INVARIANT=1" >> /etc/profile.d/dotnet.sh
RUN echo "export ASPNETCORE_ENVIRONMENT=Development" >> /etc/profile.d/dotnet.sh
RUN echo "# Add .NET Core SDK tools" >> /etc/profile.d/dotnet.sh
RUN echo "export PATH=\$PATH:/root/.dotnet/tools" >> /etc/profile.d/dotnet.sh
RUN sh /etc/profile.d/dotnet.sh

# update dotnet ef commamd
# RUN dotnet tool update --global dotnet-ef

# RUN npm install -g npm-check-updates
# RUN npm update