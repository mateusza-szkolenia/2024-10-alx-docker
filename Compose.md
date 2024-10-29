# MariaDB

```
# Use root/example as user/password credentials
version: '3.1'

services:

  db:
    image: mariadb
    restart: always
    environment:
      MARIADB_ROOT_PASSWORD: example
    volumes:
      - db_data:/var/lib/mysql

  adminer:
    image: adminer
    restart: always
    ports:
      - 8080:8080

volumes:
  db_data:
```


Instalacja `apt-get install docker-compose`

Uruchomienie: `docker-compose up -d`

