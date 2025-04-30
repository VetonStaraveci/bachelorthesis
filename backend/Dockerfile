FROM python:3.9

WORKDIR /app

# Installiere Abhängigkeiten
COPY requirements.txt ./
RUN pip install --no-cache-dir -r requirements.txt

# Kopiere den Quellcode
COPY . .

# Starte den Server
CMD ["uvicorn", "main:app", "--host", "0.0.0.0", "--port", "8000"]
