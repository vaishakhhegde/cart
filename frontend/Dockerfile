#Docker file for cart frontend
#DOCKERCOMMAND OPTIONS
FROM centos:7
MAINTAINER vaishakh.hegde@gmail.com
RUN yum -y update
ADD scripts /opt
RUN chmod 755 /opt/*.sh
RUN /opt/installapache.sh
ADD code /var/www/html
ENV MY_DB_HOST_WRITE=test MY_DB_HOST_READ=test MY_DB_NAME=test MY_DB_USER=test MY_DB_PASS=test
EXPOSE 80
CMD ["/opt/startapache.sh"]