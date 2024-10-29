# 2024-10-alx-docker

Strona prowadzącego: <https://mateusza-szkolenia.github.io>

Serwer ćwiczeniowy Gitea: <https://gitea.alx.net.pl>

## Połączenie z serwerem (z Windows, macOS lub Linuksa)

- `ssh użytkownik@ad.res.i.p`

W przypadku rozłączania się połączenia dodać opcje:

- `ssh -oTCPKeepAlive=yes -oServerAliveInterval=1`

## Podstawowe polecenia Linuksa

- `sudo -i` - uruchomienie shella na prawach roota
- `passwd` - zmiana hasła
- `ip addr` - sprawdzenie adresu IP (opcja `-c` - kolor)



## Zarządzanie usługami przez `systemd`

- `systemctl status xxxx` - stan usługi
- `systemctl start xxxx` - uruchomienie usługi
- `systemctl stop xxxx` - zatrzymanie usługi
- `systemctl restart xxxx` - restart usługi (zadziała zamiast start, gdy wyłączona)
- `systemctl enable xxxx` - ustawienie startu usługi po reboocie
- `systemctl disnable xxxx` - wyłączenie startu usługi po reboocie

## Zarządzanie pakietami przez `apt` i `apt-get`

- `apt update` - aktualizacja listy pakietów
- `apt-get update` - aktualizacja listy pakietów
- `apt install xxxx` - instalacja pakietu
- `apt-get install xxxx` - instalacja pakietu
- `apt search słowo` - szukanie pakietów
- `apt-cache search słowo` - szukanie pakietów

- `dpkg -L pakiet` - wyświetlanie plików z pakietu
- `dpkg -S /sciezka/do/pliku` - wyświetlanie pakietu instalującego dany plik

## Oprogramowanie do zainstalowania

(Zarówno w kontenerze jak i VM - zależnie od potrzeby)

`apt-get install` ...

Pakiety:
- `docker.io`
- `apparmor-utils`
- `htop`
- `nano`
- `vim`
- `python3`

## fail2ban

- `fail2ban-client status sshd`

## docker

- `docer pull debian` - pobranie obrazu z rejestru
- `docker run debian /bin/cat /etc/passwd` - stworzenie kontenera i uruchomienie pojedynczego polecenia (`cat /etc/passwd`)

- `docker ps` - pokaż działające kontenery
- `docker ps --all` - pokaż wszystkie kontenery (również wyłączone)

- `docker start xxxxxx` - uruchom wyłączony kontener
- `docker attach xxxxxx` - podepnij się do głównego procesu

- `docker commit a0a0a0a0a0 nazwa/nazwa`

- `docker run -t -d -p 8001:8000 szkolenie/strona01 /usr/bin/python3 -m http.server -d /var/www` - uruchomienie aplikacji z wystawionym portem 8000 (wew) jako 8001 na publicznym IP hosta

- `docker exec -it stoic_bhaskara /bin/bash` - uruchomienie dodatkowego polecenia (procesu, np. shella) w działającym kontenerze

Skrót: `CTRL-P` `CTRL-Q` - zaby odpiąć się od "konsoli"

