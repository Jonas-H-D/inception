FROM debian:buster
RUN apt update -y
RUN apt upgrade -y
RUN apt-get install mariadb-server -y
COPY conf/50-server.cnf	/etc/mysql/mariadb.conf.d/50-server.cnf
COPY tools/mySQL.sh /etc/mysql/

RUN chmod +x /etc/mysql/mySQL.sh

ENTRYPOINT  ["sh", "/etc/mysql/mySQL.sh"]
