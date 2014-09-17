FROM jvimr/java_station:latest
MAINTAINER Jindrich Vimr <jindrich@vimr.cz>

USER root
ENV HOME /root
ENV WORKDIR /root

ADD flexibee.list /etc/apt/sources.list.d/
ADD postgresql.list /etc/apt/sources.list.d/
RUN wget --quiet -O - https://www.postgresql.org/media/keys/ACCC4CF8.asc | sudo apt-key add -
RUN apt-key adv --keyserver keyserver.ubuntu.com --recv-keys 70E18E2B
RUN apt-get -qq update && apt-get -qqy install software-properties-common
RUN apt-get -qqy install flexibee



#USER work

#ENV HOME /home/work

#WORKDIR /home/work



