# ISTQB Lern-Quiz

Ein schlankes, offline nutzbares Lern-Quiz zur Prüfungsvorbereitung auf den
ISTQB Certified Tester Foundation Level. Die App besteht aus einer einzigen
HTML-Datei und läuft ohne Server direkt im Browser – auf dem Desktop wie auf
dem Handy.

## Nutzung

`index.html` per Doppelklick im Browser öffnen. Es ist keine Installation und
kein Server nötig. Auf dem Handy lässt sich die Datei über einen Dateimanager
oder einen Cloud-Dienst öffnen.

## Funktionen

- Fragen mit anklickbaren Antwortoptionen (Einfach- und Mehrfachauswahl)
- Anzeige der korrekten Lösung samt ausführlicher Erklärung
- Drei Modi: der Reihe nach, zufällig, oder gezielt nach Fragennummer
- Filter nach Schwierigkeitslevel (1–5)
- Vor- und Zurückblättern in allen Modi
- Fortschritts- und Trefferanzeige mit Abschluss-Zusammenfassung

## Aufbau

Das Projekt ist bewusst minimal gehalten:

- `index.html` – die komplette App (HTML, CSS, JavaScript in einer Datei).
  Die Fragen sind als JavaScript-Array `fragen` im `<script>`-Block eingebettet.
- `PROJEKT.md` – kurze Übersicht der Grundpfeiler und Konventionen.
- `.gitignore`, `.gitattributes` – Git-Konfiguration.

## Fragen pflegen

Neue Fragen werden im `fragen`-Array in `index.html` ergänzt, zwischen den
Kommentarmarkierungen `HIER NEUE FRAGEN EINFÜGEN` und `ENDE FRAGEN-ARRAY`.

Jede Frage hat folgendes Format:

```javascript
{
  id: 1,
  level: 1,
  typ: "mc",          // "mc" = Multiple Choice, "wf" = Wahr/Falsch
  frage: "Fragetext …",
  optionen: { A: "…", B: "…", C: "…", D: "…", E: "…", F: "…" },
  loesung: "B",        // ein Buchstabe, oder mehrere wie "AC"
  erklaerung: "Erklärungstext …"
}
```

Ein Platzhalter für ein gesuchtes Wort in Lückentext-Fragen wird einheitlich
als `_______` (sieben Unterstriche) geschrieben.

Beim Öffnen der Datei prüft die App die Daten automatisch und meldet mögliche
Probleme (z. B. doppelte IDs) in der Browser-Konsole (F12).

## Stand

Ziel sind 500 Fragen, verteilt auf fünf Level (je 100). Der Fortschritt der
Erfassung wird laufend ergänzt.
