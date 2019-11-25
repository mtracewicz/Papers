# __Docker__

### Przygotował Michał Tracewicz

---

## Spis treści

1. [Wstęp](#Wstęp)
2. [Instalacja](#Instalacja)
3. [Kontenery](#Kontenery)
4. [Docker file](#Docker-file)
5. [Docker compose](#Docker-compose)
6. [Bibliografia](#Bibliografia)

---

## Wstęp

### Czym jest docker i do czego służy?

Docker jest narzędziem służącym do wirtualizacji na poziomie systemu operacyjnego. Jego głównym zastosowaniem jest uniezależnienie środowiska uruchomieniowego naszej aplikacji od systemu operacyjnego na którym pracujemy oraz bibliotek, framworków etc., które są na nim zainstalowane. Co za tym idzie możemy w stosunkowo łatwy sposób pozbyć się klasycznego problemu "A u mnie działa.".  Dodatkowo pozwala to na uniknięcie dużej liczby problemów przy przenoszeniu naszej aplikacji ze środowiska produkcyjnego do środowiska produkcyjnego. 

### Czym docker nie jest.

Docker nie jest maszyną wirtualną. Jego celem nie jest symulowanie działania pełnego systemu operacyjnego  np. w celu używania jako środowiska programistycznego, używania IDE etc. a jedynie bycie nakładką na obecnie używany system operacyjny.

### Dlaczego docker a nie maszyna wirtualna

Konteneryzacja pozwala nam na znaczną oszczędność miejsca na dysku, przyśpieszyć wykonanie aplikacji (nie musimy poświęcać zasobów naszego komputera na obsługę systemu operacyjnego) oraz ułatwienie procesu uruchomiania aplikacji i możliwość skalowania horyzontalnego.

### Wizualna reprezentacja różnicy

|                         __Kontener__                         |                    __Maszyna wirtualne__                     |
| :----------------------------------------------------------: | :----------------------------------------------------------: |
| <img src="/home/mtracewicz/Documents/Papers/Docker/Container@2x.png" style="zoom:25%;" /> | <img src="/home/mtracewicz/Documents/Papers/Docker/VM@2x.png" style="zoom:25%;" /> |

Obrazki pochodzą ze strony: https://docs.docker.com/get-started/

---

##  Instalacja

### Linux (Manjaro)

```bash
sudo pacman -S docker
sudo pacman -S docker-compose
sudo usermod -aG docker $USER
sudo systemctl enable docker
```

następnie restartujemy komputer.

### Windows 10 (Wersje Pro, Education,  Enterprise)

Zanim zaczniemy instalację musimy się upewni, że w ustawieniach BIOS mamy włączoną wirtualizację sprzętową.

Aby zainstalować dockera na systemie Windows 10 należy wejść na stronę [dockera](https://www.docker.com/products/docker-desktop) następnie zarejestrować się i pobrać  aplikację docker desktop.  Dodatkowo musimy  włączyć następujące funkcje systemu Windows :

* Hyper-V
* Kontenery Windows

---

## Kontenery

### Obrazy

W dockerze przepisy na to jak postawić daną aplikację nazywamy obrazami.

#### Skąd je wziąć?

##### DockerHub

##### Budowanie

#### Listowanie obrazów

```bash
docker images
```

#### Usuwanie obrazów

```bash
docker rmi nazwa-obrazu
```

### Zarządzanie kontenerami

#### Jak uruchomić kontener

Najprostszym sposobem jest użycie plecenia "docker run"

```bash
docker run hello-world
```

#### Zachowywanie zmian w kontenerze

#### Usuwanie kontenera

```bash
docker rm id-kontenera
```

---

## Docker file

### Składnia

---

## Docker Compose

---

## Bibliografia

### Wstęp

* https://docs.docker.com/engine/docker-overview/
* https://docs.docker.com/get-started/
* https://djangoforprofessionals.com/docker/

### Instalacja

#### Manjaro

* https://gamblisfx.com/install-docker-on-manjaro-linux/
* https://manjaro.site/how-to-install-docker-on-manjaro-18-0/

#### Windows

* https://docs.docker.com/docker-for-windows/install/

### Kontenery

### Docker file

### Docker Compose