FROM centos:centos6
MAINTAINER Alex Wiechert <awiechert@elastic2ls.com>
ENV DEBIAN_FRONTEND noninteractive
RUN yum -y update; yum clean all
RUN yum -y install epel-release; yum clean all
RUN yum -y install supervisor curl net-tools mlocate nano vim less httpd mod_ssl mod_rewrite
CMD ["/usr/sbin/apachectl", "-D", "FOREGROUND"]
EXPOSE 80 443

