FROM debian

RUN apt-get update
RUN apt-get -y install tzdata
RUN apt-get -y install apache2

ADD moja_strona /var/www/html

CMD ["/usr/sbin/apachectl", "-D", "FOREGROUND"]

