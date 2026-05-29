# lernatelier-public

Öffentliche Seite des Lernatelier-Dashboards.

Enthält ausschliesslich anonymisierte Daten der Lernenden (UUID, Compliance-Status).
**Keine Namen, keine Klassen, keine Repository-URLs.**

## Studenten-Link

```
https://djlauk.github.io/lernatelier-public/student.html?uuid=<UUID>
```

Der Link wird einmalig per E-Mail zugestellt.

## Inhalt

```
student.html          Einzelne Seite für alle Lernenden (UUID via ?uuid=)
students/
  {uuid}.json         Anonymisierte Statusdaten je Lernende:r
```

## Deployment

Wird automatisch durch den GitHub Action in `lernatelier-mgmt` befüllt.
Manuelles Editieren ist nicht nötig.

## Lokales Ausprobieren

```
uv venv    # oder: python -m venv create .venv
.venv/scripts/activate
python -m http.server 8001
```
Dann läuft der Webserver lokal und ist erreichbar unter: http://localhost:8001/student.html

## GitHub Pages einrichten

Settings → Pages → Source: Deploy from branch `main`, folder `/` (root)
