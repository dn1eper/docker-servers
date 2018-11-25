FROM centos:latest

RUN yum -y update && \
    yum -y install epel-release && \
    yum install -y httpd && \
    yum install -y nginx

RUN mkdir -p /var/www/html/forbidden && \
    mkdir /var/www/html/admin && \ 
    mkdir /var/www/html/logs && \
    mkdir /var/cache/nginx

RUN htpasswd -cb /etc/nginx/.htpasswd admin admin

COPY nginx.conf /etc/nginx/
COPY my.conf    /etc/nginx/conf.d/
COPY index.html /var/www/html/

CMD  ["nginx", "-g", "daemon off;"]

EXPOSE 80
