FROM ubuntu:latest
MAINTAINER Jindrich Vimr <jindrich@vimr.cz>


RUN apt-get -qq update
RUN apt-get -qqy install ruby ruby-dev git vim wget curl sudo gawk g++ make libreadline6-dev zlib1g-dev libssl-dev libyaml-dev libsqlite3-dev sqlite3 autoconf libgdbm-dev libncurses5-dev automake libtool bison pkg-config libffi-dev


RUN useradd -m work


RUN mkdir -p /home/work/.ssh /home/work/src

ADD authorized_keys /home/work/.ssh/

COPY .gitconfig /home/work/

RUN chown -R work:work /home/work/.ssh  /home/work/.gitconfig /home/work/src/

RUN echo "work ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/work


#USER work
#WORKDIR /home/work
#ENV HOME /home/work





