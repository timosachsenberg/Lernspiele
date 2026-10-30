# Lernspiele

Kleine Lernspiele für die Grundschule. Sie laufen im Browser, ohne Anmeldung, ohne Build-Schritt und ohne externe Server.

**Spielen:** https://timosachsenberg.github.io/lernspiele/

## Spiele

| Spiel | Klasse | Fach | Inhalt |
|---|---|---|---|
| [Ohne Bremse](spiele/ohne-bremse/) | 3 | Mathe | Kopfrechnen: Plus und Minus bis 100 und bis 1000, Einmaleins, Geteilt, gemischt. Der Zug hat keine Bremse; wer richtig rechnet, stellt die Weiche auf den richtigen Tunnel. Bei der falschen Weiche gibt es einen lustigen Unfall. |

## Aufbau

```
index.html                 Auswahlseite
spiele/<name>/index.html   ein Spiel pro Ordner, eigenständige HTML-Datei
spiele/<name>/vorschau.png Vorschaubild für die Auswahlseite (16:9)
fonts/                     selbst gehostete Schriften (SIL OFL 1.1)
```

Jedes Spiel ist eine einzelne HTML-Datei mit eingebettetem CSS und JavaScript. Die Seiten laden nichts von fremden Servern; die Schriften liegen im Repo, damit keine Daten an Dritte gehen.

## Neues Spiel hinzufügen

1. Ordner `spiele/<name>/` anlegen, Spiel als `index.html` hineinlegen.
2. Schriften über `../../fonts/fonts.css` einbinden und einen Link `../../` zurück zur Auswahl setzen.
3. Ein Vorschaubild `vorschau.png` (16:9, etwa 960 × 540) ablegen.
4. In `index.html` den Kartenblock (`<li class="game">`) kopieren und anpassen.
5. Die Tabelle oben ergänzen.

## Lokal testen

```
python3 -m http.server
```

Dann http://localhost:8000 öffnen.

## Lizenzen

Die Schriften Bungee und Nunito stehen unter der SIL Open Font License 1.1 (siehe `fonts/LICENSE-*.txt`).
