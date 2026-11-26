# Einstellungen

## settings.json

Die Datei enthält die Schalter des Panels:

| Schlüssel | Bedeutung |
|---|---|
| `PAUSED` | Bot pausiert |
| `REBIRTH_ENABLED` | Automatischer Rebirth |
| `REBIRTH_AFTER_MIN` | Minute, ab der der Rebirth startet |
| `FORGE_ENABLED` | Forge automatisch spielen |
| `FORGE_UNTIL_MIN` | Letzte Minute, in der Forge gestartet wird |
| `PLAY_AGAIN_ENABLED` | Nach „Run Over“ neues Spiel |
| `LEVEL_HEROES` | Helden leveln |

## Konstanten im Programm

| Gruppe | Beispiele |
|---|---|
| Verbindung | ADB-Pfad, Geräteadresse, Paketname |
| Takt | `LOOP_PAUSE` (Pause zwischen Runden, 1,5 s) |
| Helden | `TAPS_PER_BUTTON`, `HERO_BUTTONS`, `SCROLL_LIST`, `SCROLL_STEPS` |
| Taps | `PERIODIC_TAPS` |
| Rebirth | `TIMER_REGION`, `ANGEL`, `REBIRTH_BTN`, `DIALOG_CLOSE`, `HERO_TAB`, `CONFIRM_TIMEOUT` |
| Forge | `KRACHER`, `MENU_TOGGLE_CLOSED`, `FORGE_CLOSE`, `GAME_AREA`, AutoIt-Pfad |

Alle Koordinaten beziehen sich auf den 1600×900-Screenshot.
