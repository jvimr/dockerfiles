FROM jvimr/dev_station:latest
MAINTAINER Jindrich Vimr <jindrich@vimr.cz>


RUN apt-get -qq update
RUN apt-get -qqy install mysql-server mysql-client libmysqlclient-dev


EXPOSE 3306


ADD mysql-bind-all.cnf /etc/mysql/conf.d/
ADD mysqld_charset.cnf /etc/mysql/conf.d/mysqld_charset.cnf

RUN /etc/init.d/mysql start && /usr/bin/mysqladmin password pentium && /etc/init.d/mysql stop


# Add VOLUMEs to allow backup of config and databases
VOLUME  ["/etc/mysql", "/var/lib/mysql"]


CMD ["/bin/sh" "/usr/bin/mysqld_safe"]
