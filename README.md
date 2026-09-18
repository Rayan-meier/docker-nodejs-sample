# ToDo-Applikation mit Docker

## Projektbeschreibung

In diesem Projekt habe ich mit einer bestehenden ToDo-Applikation gearbeitet.
Zuerst habe ich die Anwendung lokal gestartet und getestet. Danach habe ich sie mit Docker in einem Container ausgeführt.

Bei der Aufgabe habe ich mit Git, GitHub, Node.js, Docker und Docker Compose gearbeitet.

## Voraussetzungen

Für das Projekt werden folgende Programme benötigt:

- Git
- Node.js
- npm
- Docker Desktop
- Visual Studio Code

## Repository klonen

Als Erstes wird das Repository von GitHub geklont:

```bash
git clone https://github.com/Rayan-meier/docker-nodejs-sample.git
```

Danach wechselt man in den Projektordner:

```bash
cd docker-nodejs-sample
```

## Pakete installieren

Nach dem Klonen müssen die benötigten Pakete installiert werden:

```bash
npm install
```

Die benötigten Pakete sind in der `package.json` eingetragen.

## Anwendung lokal starten

Die Anwendung wird lokal mit folgendem Befehl gestartet:

```bash
npm run dev
```

Danach kann die ToDo-Applikation im Browser unter `http://localhost:3000` geöffnet werden.

## Docker-Image erstellen

Bevor die Anwendung in einem Container gestartet werden kann, muss ein Docker-Image erstellt werden:

```bash
docker build -t todo-app .
```

`todo-app` ist der Name des erstellten Images.

Mit folgendem Befehl kann kontrolliert werden, ob das Image vorhanden ist:

```bash
docker image ls
```

## Anwendung mit Docker starten

Aus dem Image wird mit folgendem Befehl ein Container gestartet:

```bash
docker run --name todo-container -p 3000:3000 todo-app
```

Die Angabe `3000:3000` verbindet Port 3000 auf meinem Computer mit Port 3000 im Container.

Danach ist die Anwendung wieder unter `http://localhost:3000` erreichbar.

## Docker-Container kontrollieren

Mit folgendem Befehl kann ich kontrollieren, ob der Container läuft:

```bash
docker ps
```

## Docker-Container stoppen und entfernen

Der Container wird so gestoppt:

```bash
docker stop todo-container
```

Danach kann er entfernt werden:

```bash
docker rm todo-container
```

## Anwendung mit Docker Compose starten

Die Anwendung kann auch mit Docker Compose gestartet werden:

```bash
docker compose up --build
```

Damit der Container im Hintergrund läuft, wird folgender Befehl verwendet:

```bash
docker compose up -d
```

Mit diesem Befehl kann der Status kontrolliert werden:

```bash
docker compose ps
```

## Änderung am Quellcode testen

Ich habe einen sichtbaren Text in der ToDo-Anwendung geändert.

Beim Start mit:

```bash
docker compose up -d
```

wurde zuerst noch der alte Text angezeigt.

Deshalb habe ich das Docker-Image mit folgendem Befehl neu gebaut:

```bash
docker compose up -d --build
```

Danach war die Änderung auch im Browser sichtbar.

## Anwendung mit Docker Compose stoppen

Docker Compose wird mit folgendem Befehl beendet:

```bash
docker compose down
```

## Kurzer Ablauf

1. Repository klonen.
2. Pakete installieren.
3. Anwendung lokal testen.
4. Docker-Image erstellen.
5. Container starten und testen.
6. Docker Compose verwenden.
7. Änderungen mit Git speichern und auf GitHub pushen.

*Ein Docker-Image ist die Vorlage für die Anwendung. Ein Container ist eine laufende Instanz von diesem Image.*

Weitere Informationen zu Docker gibt es in der [Docker-Dokumentation](https://docs.docker.com/).