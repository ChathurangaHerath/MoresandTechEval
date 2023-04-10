FROM centos

RUN yum -y update
RUN yum -y install nginx

COPY default ~/nginx-docker/sites
VOLUME ~/nginx-docker

EXPOSE 80/tcp

CMD ["/usr/sbin/nginx", "-g", "daemon off;"]
