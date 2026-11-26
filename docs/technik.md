# Technik

## ADB

Screenshots kommen per `adb exec-out screencap`, Taps und Wischgesten per `adb shell input`. Der Bot kennt Funktionen für Screenshot, Tap, Swipe und die Prüfung, ob das Spiel im Vordergrund ist.

## Bilderkennung

- **Button aktiv?** Ein Farbvergleich an einer festen Stelle: Ein bezahlbarer „+1“-Button ist braun und gesättigt, ein nicht bezahlbarer grau.
- **Grün?** Prüfung (per Median, damit die weiße Schrift nicht stört), ob an der Stelle die grüne Farbe des Rebirth-Buttons liegt.
- **Symbol sichtbar?** Vorlagenvergleich (zum Beispiel das Konfetti-Symbol im Seitenmenü).
- **Ergebnisbildschirm?** Prüfung auf „Run Over“ im Spielbereich.

## Texterkennung

Der Timer wird über die **Windows-OCR** (`winocr`) gelesen. Die Sprache der Erkennung ist Deutsch. Der Bildausschnitt wird vorher vergrößert, damit kleine Ziffern sicher erkannt werden. Ein Wortsuch-Hilfsmittel findet bestimmte Wörter im Bild, zum Beispiel „Confirm“.

## Forge-Skript

Der Bot startet und beendet das AutoIt-Skript und schaltet dessen automatische Wiedergabe über die INI. Ob das Skript läuft, weiß er über den gestarteten Prozess.

## Protokoll

Der Bot gibt seine Schritte als Text aus. Der aktuelle Status steht im Panel („startet …“, aktuelle Aktion).
