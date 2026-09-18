# ToDo-Applikation mit Docker

## Projektbeschreibung

Dieses Projekt ist eine einfache ToDo-Applikation mit Node.js.
Mit der Anwendung können ToDo-Einträge erstellt und verwaltet werden.

Im Projekt werden Git, GitHub, Markdown und Docker verwendet.
Die Anwendung kann lokal oder später in einem Docker-Container gestartet werden.

## Voraussetzungen

Für dieses Projekt werden folgende Programme benötigt:

- Git
- Node.js
- npm
- Docker Desktop
- Visual Studio Code
## Repository klonen

Das Repository kann mit folgendem Befehl geklont werden:

```bash
git clone https://github.com/Rayan-meier/docker-nodejs-sample.git
```

Danach in den Projektordner wechseln:

```bash
cd docker-nodejs-sample
```

## Pakete installieren

Die benötigten Pakete werden mit folgendem Befehl installiert:

```bash
npm install
```
## Anwendung lokal starten

Die Anwendung wird mit folgendem Befehl gestartet:

```bash
npm run dev
```

Anschliessend kann die ToDo-Applikation im Browser unter `http://localhost:3000` geöffnet werden.
## Docker-Image erstellen

Das Docker-Image wird mit folgendem Befehl erstellt:

```bash
docker build -t todo-app .
```

Mit diesem Befehl wird aus dem Dockerfile das Image `todo-app` erstellt.

## Anwendung mit Docker starten

Der Docker-Container wird mit folgendem Befehl gestartet:

```bash
docker run --name todo-container -p 3000:3000 todo-app
```

Danach ist die ToDo-Applikation im Browser unter `http://localhost:3000` erreichbar.

Der Container kann mit folgenden Befehlen gestoppt und entfernt werden:

```bash
docker stop todo-container
docker rm todo-container
```
## Anwendung mit Docker Compose starten

Die Anwendung kann mit Docker Compose gestartet werden:

```bash
docker compose up --build
```

Die Anwendung kann auch im Hintergrund gestartet werden:

```bash
docker compose up -d
```

Nach Änderungen am Quellcode muss das Docker-Image neu gebaut werden:

```bash
docker compose up -d --build
```

## Anwendung stoppen

Docker Compose wird mit folgendem Befehl gestoppt:

```bash
docker compose down
```

**Hinweis:** Mit `--build` wird das Docker-Image neu erstellt, damit Änderungen am Quellcode übernommen werden.