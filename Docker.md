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

## Caddy na Debianie

(użycie wersji caddy z repo debiana)

```dockerfile
FROM debian

RUN apt-get update
RUN apt-get -y install tzdata
RUN apt-get -y install caddy
RUN apt-get -y install ca-certificates

ADD moja_strona /usr/share/caddy

CMD ["/usr/bin/caddy", "run", "--environ", "--config", "/etc/caddy/Caddyfile"]
```

Aby Caddy serwował stronę po HTTPS z poprawnym certyfikatem:

```caddyfile
mateusza.alx.net.pl {
	root * /strona
	file_server
}
```

(przy uruchamianiu kontenera publikujemy porty 80 i 443: `-p 80:80 -p 443:443`)

