import tkinter as tk
from datetime import datetime, timedelta

def berechne_feierabend():
    try:
        start = datetime.strptime(eingabe.get(), "%H:%M")
        arbeitszeit = timedelta(hours=8, minutes=30)
        feierabend = start + arbeitszeit
        ergebnis_label.config(
            text=f"Feierabend: {feierabend.strftime('%H:%M')}",
            fg="#00ffcc"
        )
    except ValueError:
        ergebnis_label.config(
            text="❌ Format: HH:MM",
            fg="#ff5555"
        )

def update_uhr():
    jetzt = datetime.now().strftime("%H:%M:%S")
    uhr_label.config(text=f"Aktuelle Zeit: {jetzt}")
    fenster.after(1000, update_uhr)

# Fenster
fenster = tk.Tk()
fenster.title("Work Time System")
fenster.geometry("380x260")
fenster.configure(bg="#0f172a")
fenster.resizable(False, False)

# Titel
tk.Label(
    fenster,
    text="⏱ WORK TIME SYSTEM",
    font=("Segoe UI", 16, "bold"),
    fg="#38bdf8",
    bg="#0f172a"
).pack(pady=10)

# Live Uhr
uhr_label = tk.Label(
    fenster,
    font=("Consolas", 12),
    fg="#a5f3fc",
    bg="#0f172a"
)
uhr_label.pack()

# Eingabe
eingabe = tk.Entry(
    fenster,
    font=("Consolas", 14),
    justify="center",
    bg="#020617",
    fg="#e5e7eb",
    insertbackground="white",
    relief="flat"
)
eingabe.pack(pady=10)
eingabe.insert(0, "00:00")

# Button
tk.Button(
    fenster,
    text="BERECHNEN",
    command=berechne_feierabend,
    font=("Segoe UI", 12, "bold"),
    bg="#22d3ee",
    fg="#020617",
    relief="flat",
    activebackground="#67e8f9"
).pack(pady=10)

# Ergebnis
ergebnis_label = tk.Label(
    fenster,
    text="Feierabend: --:--",
    font=("Consolas", 14),
    fg="#00ffcc",
    bg="#0f172a"
)
ergebnis_label.pack(pady=10)

# Uhr starten
update_uhr()

fenster.mainloop()
