# Runbook: Disaster Recovery

## Wann anwenden

Server nicht mehr erreichbar, OS neu installiert, kompletter Datenverlust.

## Voraussetzungen

- [ ] Zugang zu Backups
- [ ] Neues OS installiert (oder altes wieder erreichbar)
- [ ] SSH funktioniert

## Schritte

1. **Docker installieren**
   ```bash
   curl -fsSL https://get.docker.com | sh
   sudo usermod -aG docker $USER
   ```

2. **Repos klonen**
   ```bash
   mkdir -p ~/Claude
   cd ~/Claude
   git clone git@github.com:sheep64/homelab-wiki.git
   # weitere Repos...
   ```

3. **`.env`-Dateien aus Backup wiederherstellen**
   ```bash
   # Secrets sind NICHT im Git — aus Backup/Passwort-Manager holen
   ```

4. **Services starten**
   ```bash
   cd homelab-wiki && docker compose up -d
   # weitere Services...
   ```

5. **Alle Services prüfen** — `docs/index.md` als Checkliste nutzen.

## Erfolgskriterium

Alle Services in `docs/index.md` zeigen 🟢.

## Wichtige Backups die existieren müssen

| Was | Wo gesichert |
|---|---|
| `.env`-Dateien | _ausfüllen_ |
| SQLite-Datenbanken | _ausfüllen_ |
| Konfigurationsdateien | _ausfüllen_ |
