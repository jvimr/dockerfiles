FROM jvimr/dev_station:latest
MAINTAINER Jindrich Vimr <jindrich@vimr.cz>

RUN apt-get -qq update && apt-get -qqy install software-properties-common
RUN add-apt-repository -y ppa:webupd8team/java && apt-get -qq update

RUN echo oracle-java7-installer shared/accepted-oracle-license-v1-1 select true | sudo /usr/bin/debconf-set-selections

RUN apt-get -qqy install oracle-java7-set-default

USER work

ENV HOME /home/work

WORKDIR /home/work

