# Einrichtung

## Voraussetzungen

- **Windows** mit **MuMu Player** (Netease), ADB aktiviert
- **Python** mit OpenCV, NumPy und `winocr` (Windows-Texterkennung)
- **AutoIt** für das Relic-Forge-Skript
- Das Spiel EF2 (Paketname `com.ekkorr.ef2.gb`) im Emulator, **Querformat**, Screenshot-Auflösung **1600×900**

## Verbindung

Der Bot verbindet sich über ADB mit dem Emulator (`127.0.0.1:16384`). Der Pfad zu `adb.exe` ist als Konstante hinterlegt (im MuMu-Ordner unter `nx_main`).

## Erster Start

1. Emulator starten und das Spiel öffnen.
2. `python bot.py shot` aufrufen: Es entsteht `shots/latest.png`. Stimmt die Auflösung (1600×900), kann es losgehen.
3. `python bot.py once` führt genau eine Runde aus, zum Testen.
4. `python bot.py` startet die Schleife. Strg+C beendet.
5. Das Kontrollpanel mit Numpad 0 einblenden.

## Dateien

| Datei | Zweck |
|---|---|
| `bot.py` | Hauptschleife |
| `panel.py` | Kontrollfenster |
| `settings.json` | Gespeicherte Schalter |
| `forge/` | Relic-Forge-Skript und seine Konfiguration |
| `shots/` | Screenshots (latest, Menü, Timer) |
| `tpl/` | Bildvorlagen zum Wiedererkennen von Symbolen |
