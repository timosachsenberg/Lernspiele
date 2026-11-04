# Lernspiele

Kleine Lernspiele für Grundschule und Unterstufe. Sie laufen im Browser, ohne Anmeldung, ohne Build-Schritt und ohne externe Server.

**Spielen:** https://timosachsenberg.github.io/Lernspiele/

## Spiele

| Spiel | Klasse | Fach | Inhalt |
|---|---|---|---|
| [Ohne Bremse](spiele/ohne-bremse/) | 3 | Mathe | Kopfrechnen im Zahlenraum bis 100 (Plus und Minus, Einmaleins, Geteilt) und bis 1000 (Plus und Minus, Ergänzen, Mal und Geteilt mit Zehnern, Verdoppeln und Halbieren, Runden). Der Zug hat keine Bremse; wer richtig rechnet, stellt die Weiche auf den richtigen Tunnel. Bei der falschen Weiche gibt es einen von zwölf Unfällen, vom Heuhaufen bis zum UFO. |
| [Vokabel-Jagd](spiele/vokabel-jagd/) | 5 | Englisch | Englisch-Vokabeln (Gymnasium, 1. Lernjahr) mit Karteikarten, Quiz, Hören, Sprechen (Aussprache-Check per Mikrofon), Paare finden, Buchstabieren und Wortliste. Sterne und Tier-Sticker als Belohnung; der Fortschritt bleibt im Browser des Geräts gespeichert. |

## Aufbau

```
index.html                 Auswahlseite
spiele/<name>/index.html   ein Spiel pro Ordner, eigenständige HTML-Datei
spiele/<name>/vorschau.png Vorschaubild für die Auswahlseite (16:9)
fonts/                     selbst gehostete Schriften (SIL OFL 1.1)
```

Jedes Spiel ist eine einzelne HTML-Datei mit eingebettetem CSS und JavaScript. Die Seiten laden nichts von fremden Servern; die Schriften liegen im Repo, damit keine Daten an Dritte gehen.

Ausnahme: Der Modus „Sprich mit!“ in der Vokabel-Jagd nutzt die Spracherkennung des Browsers. Chrome und Edge schicken die Aufnahme dafür an Google bzw. Microsoft, Safari an Apple. Das Mikrofon läuft nur, solange man aufs Mikrofon getippt hat. Firefox unterstützt den Modus nicht.

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

Die Schriften Bungee, Nunito und Baloo 2 stehen unter der SIL Open Font License 1.1 (siehe `fonts/LICENSE-*.txt`).
