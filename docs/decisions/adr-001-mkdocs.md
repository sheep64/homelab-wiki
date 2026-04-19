# ADR-001: Wiki mit MkDocs Material

**Datum:** 2026-04-19
**Status:** Entschieden

## Entscheidung

MkDocs Material wird als Wiki-Plattform verwendet.

## Kontext

Ein durchsuchbares, versioniertes Homelab-Wiki wird benötigt.
Browser-basiertes Editing ist kein Muss — Dateien werden im Editor oder via Claude Code gepflegt.

## Alternativen verworfen

| Option | Warum nicht |
|---|---|
| Wiki.js | Braucht eigene DB, viel mehr Overhead |
| BookStack | PHP + MySQL, unnötig komplex für Solo-Betrieb |
| Notion | Cloud, Privacy, Abo |
| Confluence | Kostenpflichtig |

## Konsequenzen

- ✅ Markdown-Dateien = direkt in Git versionierbar
- ✅ Ein Docker-Container, keine Datenbank
- ✅ Volltext-Suche lokal, kein Server nötig
- ✅ Live-Reload beim Schreiben
- ⚠️ Kein Browser-Editing — Änderungen nur via Dateisystem
