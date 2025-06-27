# Basis-Image mit Python
FROM python:3.10-slim

# System-Abhängigkeiten
RUN apt-get update && apt-get install -y --no-install-recommends \
    build-essential \
    git \
    curl \
  && rm -rf /var/lib/apt/lists/*

# Arbeitsverzeichnis
WORKDIR /workspace

# Python-Abhängigkeiten kopieren und installieren
COPY requirements.txt .
RUN pip install --upgrade pip \
 && pip install -r requirements.txt

# Jupyter-Port freigeben
EXPOSE 8888

# Dev-User anlegen
RUN useradd -m devuser

# Zum Dev-User wechseln
USER devuser

# Standard-Command
CMD ["bash"]