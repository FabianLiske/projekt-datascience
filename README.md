# Data Science Dev Container Template

## A. Was muss angepasst werden

**Dockerfile:**
Passe bei Bedarf Basis-Image, Python-Version und Systempakete an.

**devcontainer.json:**
- `name:` Ändere den Container-Namen.
- `forwardPorts:` Füge Ports hinzu oder entferne sie (z. B. für HTTP-Server).
- `mounts:` Passe Bind-Mounts für data/, src/ oder weitere Verzeichnisse an.
- `postCreateCommand:` Ersetze oder ergänze Installationsskripte.

**requirements.txt:**
Aktualisiere Paketliste und Versionen entsprechend deinem Projekt.

**.gitignore:**
Ergänze oder entferne Pfade, die nicht versioniert werden sollen.

## B. Verzeichnisstruktur im Container
```
/workspace/
├─ data/        # Rohdaten (nicht versioniert)
├─ src/         # Python-Module & Skripte
├─ notebooks/   # Jupyter-Notebooks
├─ requirements.txt
└─ .devcontainer/
```

## C. Anleitung zum Ausführen
1. **VS Code öffnen** Öffne das Projekt-Verzeichnis in VS Code.
2. **Dev Container starten** Drücke F1 → Remote-Containers: Reopen in Container. VS Code baut und verbindet sich automatisch.
3. **Abhängigkeiten** Alle Pakete aus requirements.txt wurden beim Container-Build installiert.
4. **Jupyter starten** Jupyter startet automatisch. Die URL aus dem Terminalhat beeits das Login-Token.

## D. Arbeiten & Versionieren
Schreibe Code in src/ und erstelle oder bearbeite Notebooks in notebooks/.
Speichern läuft automatisch über das Bind-Mount ins Host-Repo.
Committe alle Änderungen wie gewohnt mit Git.