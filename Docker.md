Przykładowy Dockerfile:

```dockerfile
FROM debian

RUN apt-get update
RUN apt-get -y install tzdata
RUN apt-get -y install apache2

RUN echo "<h1>Moja strona numer 2</h2>" > /var/www/html/index.html

CMD ["/usr/sbin/apachectl", "-D", "FOREGROUND"]

```

Budowanie: `docker build -t szkolenie/strona02:latest ./`

Aby wrzucić do obrazu pliki i katalogi:

```dockerfile
FROM debian

RUN apt-get update
RUN apt-get -y install tzdata
RUN apt-get -y install apache2

ADD moja_strona /var/www/html

CMD ["/usr/sbin/apachectl", "-D", "FOREGROUND"]
```
