Image obsahujici Javu a fio-api-plus aplikaci (viz http://www.fio.cz/bankovni-sluzby/api-bankovnictvi )

pouziti:
=======
1 do adresare cfg ulozit konfiguracni soubor fio-api-plus (napr. spustit si jednou tuto aplikaci jako GUI a spustit konfiguraci
2 sestavit image
```
 sudo docker build -t="my.fio_api_plus" ./
```
3 spustit image:
```
 sudo docker run -v `pwd`/cfg/:/home/work/cfg/ -v `pwd`/vypisy/:/home/work/vypisy/ my.fio_api_plus
```

pripadne spustit rovnou existujici image:
```
sudo docker run -v `pwd`/cfg/:/home/work/cfg/ -v `pwd`/vypisy/:/home/work/vypisy/ jvimr/fio_api_plus
```

