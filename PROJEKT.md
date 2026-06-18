# Projektübersicht & Grundpfeiler

Diese Datei hält die Leitplanken des Projekts fest. Sie ist kurz und soll
kurz bleiben.

## Ziel

Ein einfaches, fehlerfreies Lern-Quiz für die ISTQB-Foundation-Level-Prüfung,
mit 500 Übungsfragen und ausführlichen Erklärungen.

## Grundpfeiler

1. **Eine Datei.** Die gesamte App lebt in `index.html` (HTML + CSS + JS).
   Keine externen Abhängigkeiten, kein Build-Schritt, kein Server.
2. **Offline & überall.** Per Doppelklick im Browser lauffähig, auch auf dem
   Handy.
3. **Einfachheit vor Umfang.** Funktionen werden nur ergänzt, wenn sie klaren
   Nutzen bringen. Das Projekt soll abgeschlossen werden, nicht endlos wachsen.
4. **Daten getrennt denken.** Die Fragen liegen als `fragen`-Array klar
   abgegrenzt im Code und folgen einem festen Format (siehe README).
5. **Korrektheit.** Jede Änderung bleibt syntaktisch fehlerfrei; Lösungen
   müssen auf vorhandene Optionen verweisen; IDs sind eindeutig.

## Konventionen

- **Fragenformat:** `id`, `level` (1–5), `typ` ("mc"/"wf"), `frage`,
  `optionen` (A–F), `loesung`, `erklaerung`.
- **Lückentext-Platzhalter:** einheitlich `_______` (sieben Unterstriche).
- **Originaltreue:** Fragetexte werden wie in der Vorlage erfasst; auffällige
  Druckfehler werden einzeln abgestimmt, nicht stillschweigend geändert.
- **Zeilenenden:** im Repository LF (siehe `.gitattributes`).

## Definition of Done

Das Projekt gilt als fertig, wenn alle 500 Fragen erfasst sind und die App
in allen Modi fehlerfrei bedienbar ist: Frage anzeigen, antworten, Lösung und
Erklärung sehen, blättern, filtern – ohne Fehlverhalten.

## Rollen

- **Fragenerfassung & Datenpflege:** über den Assistenten (liefert geprüfte
  Blöcke fürs `fragen`-Array).
- **App-Änderungen & Git:** über die Entwicklungsumgebung (Cursor).
