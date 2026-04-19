# Docker Cheatsheet

## Container-Management

```bash
docker ps                          # Laufende Container
docker ps -a                       # Alle Container inkl. gestoppte
docker logs -f <name>              # Live-Logs
docker exec -it <name> bash        # Shell in Container
docker stats                       # CPU/RAM-Auslastung live
```

## Compose

```bash
docker compose up -d               # Starten (detached)
docker compose up -d --build       # Starten + neu bauen
docker compose down                # Stoppen + Container entfernen
docker compose restart <service>   # Einzelnen Service neustarten
docker compose ps                  # Status aller Services
docker compose logs -f <service>   # Logs eines Services
```

## Images & Cleanup

```bash
docker images                      # Alle Images
docker pull <image>:<tag>          # Image aktualisieren
docker image prune                 # Ungenutzte Images löschen
docker system prune                # Alles Ungenutzte löschen (vorsicht!)
```

## Volumes

```bash
docker volume ls                   # Alle Volumes
docker volume inspect <name>       # Details zu Volume
```

## Netzwerk

```bash
docker network ls                  # Alle Netzwerke
docker network inspect <name>      # Details
```
