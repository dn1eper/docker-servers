FROM centos:latest

RUN yum -y update && \
    yum -y install epel-release && \
    yum -y install php-fpm && \
    yum install -y nginx

RUN mkdir -p /var/www/html/forbidden && \
    mkdir /var/www/html/admin && \ 
    mkdir /var/www/html/logs


COPY nginx.conf /etc/nginx/
COPY my.conf    /etc/nginx/conf.d/
COPY index.php  /var/www/html/forbidden/
COPY index.php  /var/www/html/admin/

CMD php-fmp
CMD  ["nginx", "-g", "daemon off;"]

EXPOSE 80


#RUN htpasswd -cb /etc/nginx/.htpasswd admin admin


#ADD na_nginx.conf /etc/nginx/conf.d/defaul.conf

#COPY php-fpm.conf /etc/php-fpm.d/www.conf


#CMD nginx && php-fpm