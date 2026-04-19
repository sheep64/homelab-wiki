# Linux Cheatsheet

## Netzwerk

```bash
ip a                               # Alle Interfaces + IPs
ss -tlnp                           # Offene TCP-Ports + Prozesse
ping -c 4 <host>                   # Erreichbarkeit testen
curl -I <url>                      # HTTP-Header prüfen
```

## Prozesse

```bash
ps aux | grep <name>               # Prozess suchen
htop                               # Interaktiver Task-Manager
kill -9 <pid>                      # Prozess hart beenden
systemctl status <service>         # Systemd-Service-Status
journalctl -u <service> -f         # Systemd-Logs live
```

## Dateisystem

```bash
df -h                              # Festplatten-Auslastung
du -sh <dir>                       # Größe eines Verzeichnisses
ls -lah                            # Dateien mit Größe + Rechten
find /path -name "*.log"           # Dateien suchen
```

## Berechtigungen

```bash
chmod 755 <file>                   # rwxr-xr-x
chown user:group <file>            # Eigentümer ändern
sudo -i                            # Root-Shell
```

## Sonstiges

```bash
history | grep <befehl>            # Befehlshistorie durchsuchen
crontab -l                         # Aktuelle Cronjobs
watch -n 5 <befehl>               # Befehl alle 5s wiederholen
```
