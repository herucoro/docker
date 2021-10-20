FROM almalinux:latest
USER root

RUN dnf update -y
RUN yum update -y

ENV TZ JST-9
ENV TERM xterm

RUN adduser zabbix
RUN adduser postgres

RUN dnf install httpd php php-pgsql php-mbstring php-bcmath php-xml php-gd -y
RUN dnf install readline-devel zlib-devel -y

# RUN tar jxf postgresql-9.2.4.tar.bz2
# RUN cd postgresql-9.2.4
# RUN ./configure
# RUN make
# RUN su
# # make install
# # mkdir /usr/local/pgsql/data
# # chown postgres:postgres /usr/local/pgsql/data
# # su - postgres
# RUN /usr/local/pgsql/bin/initdb -D /usr/local/pgsql/data -E UTF8 --no-locale
# RUN /usr/local/pgsql/bin/pg_ctl -D /usr/local/pgsql/data -l logfile start
# RUN /usr/local/pgsql/bin/createuser -U postgres zabbix -P -S -R -D
# RUN passwod
# RUN password
# RUN /usr/local/pgsql/bin/createdb -U postgres -O zabbix -E UTF8 zabbix
# RUN exit
# # exit
# RUN cd zabbix-2.0.5
# RUN /usr/local/pgsql/bin/psql -U zabbix zabbix < database/postgresql/schema.sql
# RUN /usr/local/pgsql/bin/psql -U zabbix zabbix < database/postgresql/images.sql
# RUN /usr/local/pgsql/bin/psql -U zabbix zabbix < database/postgresql/data.sql