FROM debian

RUN apt-get update
RUN apt-get -y install tzdata
RUN apt-get -y install ca-certificates caddy

ADD Caddyfile /etc/caddy/Caddyfile.mateusza
ADD moja_strona /strona

CMD ["/usr/bin/caddy", "run", "--environ", "--config", "/etc/caddy/Caddyfile.mateusza"]

# CMD ["/usr/sbin/apachectl", "-D", "FOREGROUND"]

