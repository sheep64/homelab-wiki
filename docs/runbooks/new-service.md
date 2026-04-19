# Runbook: Neuen Service einrichten

## Wann anwenden

Immer wenn ein neuer Docker-Service auf dem Homeserver deployt wird.

## Voraussetzungen

- [ ] SSH-Zugang zum Server
- [ ] Docker + Compose läuft
- [ ] Port ist frei (`ss -tlnp | grep <port>`)

## Schritte

1. **Projektverzeichnis anlegen**
   ```bash
   mkdir -p ~/Claude/<projekt-name>
   cd ~/Claude/<projekt-name>
   ```

2. **`docker-compose.yml` erstellen** mit dem neuen Service.

3. **`.env` anlegen** für Secrets — nie Secrets in die Compose-Datei hardcoden.

4. **Container starten**
   ```bash
   docker compose up -d
   ```

5. **Logs prüfen**
   ```bash
   docker logs -f <container-name>
   ```

6. **Service-Eintrag im Wiki ergänzen**
   - `docs/index.md` → Services-Tabelle
   - `docs/services/overview.md` → Zeile hinzufügen
   - Neue Seite unter `docs/services/<name>.md` anlegen
   - `mkdocs.yml` → Nav-Eintrag hinzufügen

## Erfolgskriterium

- Container läuft: `docker ps | grep <name>`
- Service erreichbar: `curl http://localhost:<port>/health`
- Wiki-Eintrag ist aktuell

## Häufige Fehler

- **Port bereits belegt:** `ss -tlnp | grep <port>` — welcher Prozess?
- **Permission denied auf Volume:** `chown` auf das gemountete Verzeichnis prüfen
