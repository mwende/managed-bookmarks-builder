# Managed Bookmarks Builder

Ein Single-File-Web-Tool (`managed-bookmarks-builder.html`) zum Erstellen von
**Managed Bookmarks / Managed Favorites** für Google Chrome und Microsoft Edge –
für das Deployment per Microsoft Intune (oder GPO/Registry).

Aus **einem** Lesezeichen-Baum erzeugt das Tool wahlweise:

| Plattform | Browser | Ausgabe | Ziel |
|-----------|---------|---------|------|
| macOS | Chrome | plist-XML `ManagedBookmarks` | Preference file · `com.google.Chrome` |
| macOS | Edge | plist-XML `ManagedFavorites` | Preference file · `com.microsoft.Edge` |
| Windows | Chrome | JSON | Settings catalog · „Managed Bookmarks" |
| Windows | Edge | JSON | Settings catalog · „Configure favorites" |

## Features

- Baum-Editor mit Ordnern, Bookmarks, Verschieben und Live-Vorschau
- Plattform-Umschalter (macOS / Windows) und Browser-Umschalter (Chrome / Edge)
- Automatisch passende Intune-Deploy-Anleitung inkl. Registry-Pfad und OMA-URI
- Import bestehender Konfigurationen (plist-XML oder JSON) mit Auto-Erkennung
- Kein Build, keine Abhängigkeiten – einfach die HTML-Datei im Browser öffnen
- Zustand wird lokal im Browser (`localStorage`) gespeichert

## Verwendung

`managed-bookmarks-builder.html` im Browser öffnen, Baum pflegen, Plattform und
Browser wählen, generiertes Fragment kopieren und in Intune einfügen.

## Beispiel-Konfigurationen

- `wendeit.xml` – WendeIT-Favoriten für Chrome (macOS plist-XML)
- `wendeit-edge.xml` – dieselben Favoriten für Edge (macOS plist-XML)
- `ManagedBookmarks-com.google.Chrome.xml` – generisches Beispiel

---

powered by Marco Wende · WendeIT
