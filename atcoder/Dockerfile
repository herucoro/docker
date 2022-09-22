FROM ubuntu:latest

RUN apt update -y && apt install npm -y
RUN apt install python3-pip -y
RUN pip install --user online-judge-tools
RUN npm install -g atcoder-cli

RUN cp /root/.local/bin/oj bin/ && mkdir workplace