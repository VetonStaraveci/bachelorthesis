# Verwende das Node.js-Image
FROM node:16
# Setze das Arbeitsverzeichnis
WORKDIR /app
# Kopiere package.json und package-lock.json
COPY package*.json ./
# Installiere alle Abhängigkeiten
RUN npm install
# Kopiere den restlichen Code
COPY . .
# Baue die React-Anwendung
RUN npm run build
# Installiere einen Webserver
RUN npm install -g serve
# Starte den Webserver auf Port 3000
CMD ["serve", "-s", "build", "-l", "3000"]

