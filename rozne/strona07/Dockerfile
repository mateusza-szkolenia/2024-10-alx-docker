FROM debian

RUN apt-get update
RUN apt-get -y install tzdata
RUN apt-get -y install ca-certificates caddy

ADD Caddyfile /etc/caddy/Caddyfile.mateusza
RUN mkdir /strona

CMD ["/usr/bin/caddy", "run", "--environ", "--config", "/etc/caddy/Caddyfile.mateusza"]
