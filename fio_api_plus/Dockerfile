FROM jvimr/java_station:latest
MAINTAINER Jindrich Vimr <jindrich@vimr.cz>





USER work

ENV HOME /home/work

WORKDIR /home/work



RUN mkdir cfg src/fio_api_plus vypisy && cd src/fio_api_plus && wget -nv https://www.fio.cz/apps/fio_api_plus.jar

VOLUME ["/home/work/cfg/", "/home/work/vypisy/"]


CMD java -jar src/fio_api_plus/fio_api_plus.jar -set ~/cfg/ -silent
