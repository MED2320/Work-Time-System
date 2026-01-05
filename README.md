Gerne 👍
Hier ist eine **saubere, moderne README.md** passend zu deinem Projekt **„Python GUI mit Live-Uhr + Feierabend-Rechner“**.

---

# ⏱ Work Time System

Ein modernes **Python-GUI-Programm** mit **Live-Uhr**, das anhand der eingegebenen **Arbeitsbeginn-Zeit** automatisch deine **Feierabend-Zeit** berechnet.
Die tägliche Arbeitszeit ist fest auf **8,5 Stunden** eingestellt.

---

## ✨ Features

* 🕒 **Live-Uhr** (aktualisiert jede Sekunde)
* ⌨️ Einfache Eingabe des Arbeitsbeginns (HH:MM)
* 🧮 Automatische Feierabend-Berechnung
* 🌙 Modernes Dark-Design
* 🖥️ Benutzerfreundliche GUI mit **tkinter**
* 📦 Optional als **Windows .exe** nutzbar

---

## 🖼️ Vorschau (Beschreibung)

* Dunkles Fenster mit Karten-Layout
* Neon-Akzentfarben (Cyan/Blau)
* Große, gut lesbare Schrift
* Klar strukturierte Oberfläche

---

## 🛠️ Voraussetzungen

### Für die Python-Version:

* Python **3.9 oder neuer**
* Keine zusätzlichen Libraries notwendig
  (`tkinter` ist bereits enthalten)

### Für die EXE-Version:

* Windows
* `pyinstaller`

---

## ▶️ Programm starten (Python)

```bash
python work_time_system.py
```

---

## 📥 Eingabeformat

**Arbeitsbeginn:**

```
HH:MM
```

**Beispiel:**

```
07:30
```

**Ausgabe:**

```
Feierabend: 16:00
```

---

## 📦 EXE erstellen (Windows)

1️⃣ PyInstaller installieren:

```bash
pip install pyinstaller
```

2️⃣ EXE erzeugen:

```bash
pyinstaller --onefile --windowed work_time_system.py
```

3️⃣ Fertige Datei findest du unter:

```
dist/work_time_system.exe
```

✔ Kein Konsolenfenster
✔ Läuft ohne Python-Installation

---

## ⚙️ Anpassungen

Im Code kannst du leicht ändern:

* ⏱️ Arbeitszeit (Standard: 8h 30min)
* 🎨 Farben & Schriftarten
* 🕒 Uhrformat (12h / 24h)
* 📐 Fenstergröße

---

## 🚀 Ideen für Erweiterungen

* ⏸ Pausenzeit einbauen
* 💾 Letzte Startzeit speichern
* 🎨 Theme-Auswahl
* 📅 Wochenübersicht
* 🔔 Feierabend-Benachrichtigung

---

## 📄 Lizenz

Dieses Projekt ist **frei nutzbar** für private Zwecke und Lernprojekte.

