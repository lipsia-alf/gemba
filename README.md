# Gemba-Rundgang

Web-App für routinierte Gemba-Walks auf dem Shopfloor: Leitfragen, Checkliste (Sicherheit, 5S), Befunde mit Foto, Maßnahmenverfolgung, Auswertung und Excel-Export mit Fotos.

- Läuft offline nach dem ersten Öffnen.
- Alle Daten bleiben auf dem Gerät (IndexedDB). Dieses Repository enthält nur die App, keine Daten.
- Sicherung und Wiederherstellung als JSON-Datei unter „Bereiche“ → „Daten & Sicherung“.

## Dateien

| Datei | Zweck |
|---|---|
| `index.html` | die App |
| `manifest.webmanifest` | Name, Symbol und Startverhalten für „App installieren“ |
| `sw.js` | Offline-Speicher der App-Dateien |
| `icon-192.png`, `icon-512.png`, `apple-touch-icon.png` | App-Symbole |
| `vendor/exceljs.min.js` | Excel-Export (ExcelJS 4.4.0, MIT-Lizenz) |

## Updates

Geänderte Dateien hochladen und in `sw.js` die Zeile `const CACHE = "gemba-v1";` hochzählen (`gemba-v2` usw.). Die App holt die neue Fassung beim nächsten Öffnen mit Netz.
