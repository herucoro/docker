FROM ubuntu:latest

RUN apt upgrade -y && apt-get upgrade -y
RUN apt update && apt-get update
RUN apt install apache2 vim nodejs -y && apt install npm -y

ENV APACHE_RUN_USER www-data
ENV APACHE_RUN_GROUP www-data
ENV APACHE_PID_FILE /var/run/apache2.pid
ENV APACHE_RUN_DIR /var/run/apache2
ENV APACHE_LOG_DIR /var/log/apache2
ENV APACHE_LOCK_DIR /var/lock/apache2

CMD ["apachectl", "-D", "FOREGROUND"]
EXPOSE 80