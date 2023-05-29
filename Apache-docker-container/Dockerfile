FROM centos
RUN sed -i 's/mirrorlist/#mirrorlist/g' /etc/yum.repos.d/CentOS-*
RUN sed -i 's|#baseurl=http://mirror.centos.org|baseurl=http://vault.centos.org|g' /etc/yum.repos.d/CentOS-*
RUN yum update -y
RUN dnf install httpd -y
RUN dnf clean all 
COPY index.html /var/www/html/index.html
RUN chown apache:apache /var/www/html/index.html
CMD ./run.sh
