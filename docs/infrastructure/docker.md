# Docker

## Strategie

Alle Services laufen als Docker-Container und werden via `docker-compose.yml` verwaltet.
Jedes Projekt hat sein eigenes `docker-compose.yml`.

## Nützliche Befehle

```bash
# Alle laufenden Container
docker ps

# Logs eines Containers
docker logs -f <container-name>

# Container neustarten
docker compose restart <service>

# Alles stoppen
docker compose down

# Alles starten + bauen
docker compose up -d --build
```

## Volumes & Daten

_Wo liegen Daten, wie wird gesichert._
