# Idle-Bot für Endless Frontier 2 – Dokumentation

Dokumentation zu einem **Python-Hilfsprogramm**, das das Idle-Spiel Endless Frontier 2 (EF2) im Emulator **MuMu Player** über **ADB** bedient. Nur Beschreibung, kein Quellcode.

## Idee

Das Programm macht Screenshots über ADB, erkennt per Bildanalyse und Texterkennung, was auf dem Bildschirm ist, und tippt entsprechend. So laufen wiederkehrende Aufgaben im Idle-Spiel von selbst.

## Funktionen

- **Helden leveln:** erkennt aktive „+1“-Buttons in den sichtbaren Heldenzeilen und tippt sie mehrfach. Optional wird die Liste gescrollt, um auch weitere Helden zu erreichen.
- **Periodische Taps:** feste Positionen im einstellbaren Intervall, zum Beispiel für Fähigkeiten, Chat-Bonus und Wut.
- **Rebirth:** liest den Timer neben dem Stoppuhr-Symbol per Windows-OCR und startet ab einer einstellbaren Minute den Rebirth, samt Bestätigung.
- **Relic Forge:** öffnet bis zu einer einstellbaren Minute das Relic-Forge-Minispiel und startet dafür das AutoIt-Skript, das die Züge berechnet (siehe Relic-Forge-Doku). Nach „Run Over“ kann es ein neues Spiel starten.
- **Spielvordergrund:** prüft, ob das Spiel im Vordergrund ist, und holt MuMu bei Bedarf nach vorn.

## Kommandozeile

| Aufruf | Wirkung |
|---|---|
| `python bot.py` | Bot starten, Strg+C beendet |
| `python bot.py shot` | Screenshot nach `shots/latest.png` |
| `python bot.py tap X Y` | Einmal an eine Koordinate tippen |
| `python bot.py once` | Genau eine Runde, zum Testen |

Koordinaten beziehen sich auf einen Screenshot von 1600×900 im Querformat.

## Kontrollpanel

Ein kleines Fenster mit Schaltern, ein- und ausblendbar mit **Numpad 0** (NumLock an):

- Bot pausieren, Rebirth automatisch und Rebirth-Minute
- Relic Forge spielen, Forge-Minute, „Play Again“ nach Spielende
- Helden leveln
- Schalter für das Forge-Skript: Hammer automatisch, tote Relikte wegschlagen, Stern automatisch, Lernmodell

Die Schalter des Bots gelten sofort und werden in `settings.json` gespeichert. Die Forge-Schalter stehen in `RelicForge.ini` und gelten nach einem Neustart des Forge-Skripts.

## Voraussetzungen

- Windows, MuMu Player mit aktiviertem ADB
- Python mit OpenCV, NumPy und `winocr`
- AutoIt für das Forge-Skript

## Grenzen

- Alle Koordinaten sind auf eine feste Auflösung abgestimmt.
- Das Programm tippt selbstständig. Prüfe, ob die Nutzungsbedingungen des Spiels das erlauben.
