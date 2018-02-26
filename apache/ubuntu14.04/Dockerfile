FROM ubuntu:14.04
MAINTAINER Alex Wiechert <awiechert@elastic2ls.com>
RUN apt-get update
RUN apt-get install --no-install-recommends -y supervisor curl net-tools mlocate nano vim less apache2
ENV APACHE_RUN_USER www-data
ENV APACHE_RUN_GROUP www-data
ENV APACHE_LOG_DIR /var/log/apache2
CMD ["/usr/sbin/apache2ctl", "-D", "FOREGROUND"]
EXPOSE 80
