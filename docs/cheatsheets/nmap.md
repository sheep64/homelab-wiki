# nmap Cheatsheet

## Grundlegende Scans

```bash
nmap 192.168.1.1                   # Einzelne IP
nmap 192.168.1.0/24                # Ganzes Subnetz
nmap -sn 192.168.1.0/24            # Ping-Scan (nur erreichbare Hosts, keine Ports)
```

## Port-Scans

```bash
nmap -p 80,443 <host>              # Bestimmte Ports
nmap -p 1-1000 <host>              # Port-Range
nmap -p- <host>                    # Alle 65535 Ports (langsam!)
nmap -sU <host>                    # UDP-Scan
```

## Service & OS-Erkennung

```bash
nmap -sV <host>                    # Service-Versionen erkennen
nmap -O <host>                     # OS-Erkennung (benötigt root)
nmap -A <host>                     # Alles: OS + Services + Traceroute
```

## Output

```bash
nmap -oN scan.txt <host>           # In Datei speichern (normal)
nmap -oX scan.xml <host>           # XML-Output
```

!!! warning "Nur eigene Netzwerke scannen"
    nmap nur auf Netzwerke/Hosts anwenden die dir gehören oder für die du explizite Erlaubnis hast.
