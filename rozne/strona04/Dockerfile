FROM debian

RUN apt-get update
RUN apt-get -y install tzdata
RUN apt-get -y install caddy

ADD moja_strona /usr/share/caddy

CMD ["/usr/bin/caddy", "run", "--environ", "--config", "/etc/caddy/Caddyfile"]

# CMD ["/usr/sbin/apachectl", "-D", "FOREGROUND"]

