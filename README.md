# ⏱ Arbeitszeitrechner

Ein einfaches **Python-GUI-Programm** mit **Live-Uhr**, das automatisch deine **Feierabend-Zeit** basierend auf der eingegebenen Arbeitsbeginn-Zeit berechnet. Die tägliche Arbeitszeit ist auf **8,5 Stunden** festgelegt.

## ✨ Features

- 🕒 **Live-Uhr** (aktualisiert jede Sekunde)
- ⌨️ Einfache Eingabe des Arbeitsbeginns im Format HH:MM
- 🧮 Automatische Berechnung der Feierabend-Zeit
- 🌙 Modernes Dark-Design mit Neon-Akzenten
- 🖥️ Benutzerfreundliche GUI mit tkinter
- 📦 Kann als Windows .exe kompiliert werden

## 🖼️ Vorschau

Das Programm zeigt ein dunkles Fenster mit:
- Live-Uhr oben
- Eingabefeld für Arbeitsbeginn
- Berechnen-Button
- Ergebnis-Anzeige für Feierabend-Zeit

## 🛠️ Voraussetzungen

### Für Python-Version:
- Python 3.9 oder neuer
- Keine zusätzlichen Bibliotheken erforderlich (tkinter ist in Python enthalten)

### Für EXE-Version:
- Windows
- `pyinstaller` installiert

## ▶️ Programm starten

### Python-Version:
```bash
python Arbeitszeitrechner.py
```

### Eingabeformat:
- Arbeitsbeginn: `HH:MM` (z.B. `07:30`)
- Ausgabe: `Feierabend: 16:00`

## 📦 EXE erstellen (Windows)

1. PyInstaller installieren:
```bash
pip install pyinstaller
```

2. EXE erzeugen:
```bash
pyinstaller --onefile --windowed Arbeitszeitrechner.py
```

3. Die fertige EXE findest du in `dist/Arbeitszeitrechner.exe`

## ⚙️ Anpassungen

Im Code kannst du folgende Dinge ändern:
- Arbeitszeit (aktuell 8h 30min)
- Farben und Schriftarten
- Uhrformat
- Fenstergröße

## 🚀 Mögliche Erweiterungen

- Pausenzeiten berücksichtigen
- Letzte Eingabe speichern
- Mehrere Themes
- Wochenübersicht
- Benachrichtigungen

## 📄 Lizenz

Dieses Projekt ist frei für private und Bildungszwecke nutzbar.

