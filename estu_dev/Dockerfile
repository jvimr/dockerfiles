FROM jvimr/rvm_dev:latest
MAINTAINER Jindrich Vimr <jindrich@vimr.cz>

USER root
RUN apt-get -qqy update
RUN apt-get -qqy install mysql-client

USER work
WORKDIR /home/work
ENV HOME /home/work


RUN mkdir -p src/estu/

EXPOSE 3000 



RUN /bin/bash -l -c "rvm install  2.1"

RUN /bin/bash -l -c "rvm gemset use rails3217  --create"
#RUN /bin/bash -l -c "rvm gemset use  ruby-2.1.2@rails3217 --default"
RUN /bin/bash -l -c "rvm gemset list"


