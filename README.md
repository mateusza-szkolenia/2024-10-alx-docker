# 2024-10-alx-docker

Strona prowadzącego: <https://mateusza-szkolenia.github.io>

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
- 

