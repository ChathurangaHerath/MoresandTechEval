FROM mysql:latest

RUN yum -y install mysql
RUN chown -R mysql:root /var/lib/mysql/

ARG MYSQL_USER
ARG MYSQL_PASSWORD
ARG MYSQL_ROOT_PASSWORD

ENV MYSQL_USER=$MYSQL_USER
ENV MYSQL_PASSWORD=$MYSQL_PASSWORD
ENV MYSQL_ROOT_PASSWORD=$MYSQL_ROOT_PASSWORD

VOLUME ["~/mysql-docker", "/var/lib/mysql"]
WORKDIR /data/mysql/bin

COPY /etc/my.cnf ~/mysql-docker

EXPOSE 3306/tcp
CMD ["mysqld_safe"]


