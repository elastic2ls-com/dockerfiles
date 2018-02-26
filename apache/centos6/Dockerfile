FROM centos:centos6
MAINTAINER Alex Wiechert <awiechert@elastic2ls.com>
ENV DEBIAN_FRONTEND noninteractive
RUN yum -y update; yum clean all
RUN yum -y install epel-release; yum clean all
RUN yum -y install supervisor curl net-tools mlocate nano vim less httpd
CMD ["/usr/sbin/apachectl", "-D", "FOREGROUND"]
EXPOSE 80


