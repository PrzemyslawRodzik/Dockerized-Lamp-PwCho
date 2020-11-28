# Dockerized-Lamp-PwCho

### Uruchomienie

```sh
docker-compose build
docker-compose up 
```
lub 
```sh
docker-compose build
docker-compose up -d
```
Ważnym elementem, o którym należało pamiętać było skonfigurowanie serwera Apache, by żądania dotyczące plików php były przekierowywane do serwera php. 
W pliku konfiguracyjnym Apache należało dodać polecenie:
```sh
ProxyPassMatch ^/(.*\.php(/.*)?)$ fcgi://php:9000/usr/local/apache2/htdocs/$1
```
### Graficzna reprezentacja:
![docker-compose](https://s1.imghub.io/sT79t.png)
