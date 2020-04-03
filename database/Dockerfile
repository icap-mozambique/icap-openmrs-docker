FROM mysql:5.6

LABEL maintainer="sis@cumc.columbia.edu"

ENV MYSQL_ROOT_PASSWORD=root
ENV MYSQL_DATABASE=openmrs
ENV MYSQL_USER=icap
ENV MYSQL_PASSWORD=icap
ENV MYSQL_DATA_DIRECTORY=/opt/openmrs/data/system/mysql

ADD mysql.cnf /root/.my.cnf
ADD localtime /etc/localtime

COPY run.sh /run.sh

VOLUME /opt/openmrs/data

EXPOSE 3306

CMD ["/run.sh"]