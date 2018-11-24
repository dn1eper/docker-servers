FROM centos:latest

RUN yum -y update && yum -y install httpd

RUN mkdir -p /var/www/html/forbidden && \
    mkdir /var/www/html/admin && \ 
    mkdir /var/www/html/logs

COPY my.conf /etc/httpd/conf.d/
COPY .htaccess /var/www/html/

CMD /usr/sbin/httpd -DFOREGROUND

EXPOSE 80
