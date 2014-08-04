FROM jvimr/dev_station:latest
MAINTAINER Jindrich Vimr <jindrich@vimr.cz>



COPY .gitconfig /home/work/
#RUN chown work:work /home/work/.gitconfig

USER work

ENV HOME /home/work

WORKDIR /home/work





RUN curl -sSL https://get.rvm.io | bash -s stable
