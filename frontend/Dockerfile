# Verwende das Node.js-Image
FROM node:16
# Setze das Arbeitsverzeichnis
WORKDIR /app
# Kopiere package.json und package-lock.json (falls vorhanden)
COPY package*.json ./
# Installiere alle Abhängigkeiten (inklusive react-scripts)
RUN npm install
# Kopiere den restlichen Code
COPY . .
# Baue die React-Anwendung für die Produktion
RUN npm run build
# Installiere einen Webserver, um die Build-Ausgabe bereitzustellen
RUN npm install -g serve
# Starte den Webserver auf Port 3000
CMD ["serve", "-s", "build", "-l", "3000"]

