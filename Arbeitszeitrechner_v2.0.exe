import tkinter as tk
from tkinter import ttk
from datetime import datetime, timedelta

def validate_integer(char):
    """Nur Zahlen erlauben"""
    return char.isdigit() or char == ""

def berechne_feierabend():
    try:
        stunden = int(stunden_spin.get())
        minuten = int(minuten_spin.get())
        
        if stunden < 0 or stunden > 23 or minuten < 0 or minuten > 59:
            ergebnis_label.config(
                text="❌ Stunden: 0-23, Minuten: 0-59",
                fg="#ff5555"
            )
            return
        
        start = datetime.strptime(f"{stunden:02d}:{minuten:02d}", "%H:%M")
        arbeitszeit = timedelta(hours=8, minutes=30) # Standard-Arbeitszeit: 8 Stunden 30 Minuten
        feierabend = start + arbeitszeit
        ergebnis_label.config(
            text=f"Feierabend: {feierabend.strftime('%H:%M')}",
            fg="#00ffcc"
        )
    except ValueError:
        ergebnis_label.config(
            text="❌ Nur Zahlen | Stunden: 0-23, Minuten: 0-59",
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
fenster.resizable(True, True)
fenster.iconbitmap("icon/clock_icon.ico") # Optional: Füge ein Icon hinzu

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

# Eingabe - Stunden und Minuten mit Combobox
eingabe_frame = tk.Frame(fenster, bg="#151922")
eingabe_frame.pack(pady=10)

# Label für Stunden
tk.Label(
    eingabe_frame,
    text="",
    font=("Segoe UI", 11),
    fg="#38bdf8",
    bg="#0f172a"
).grid(row=0, column=0, padx=5)

# Spinbox für Stunden (0-23)
stunden_spin = tk.Spinbox(
    eingabe_frame,
    from_=0,
    to=23,
    width=4,
    font=("Consolas", 14),
    justify="center",
    bg="#020617",
    fg="#e5e7eb",
    buttonbackground="#020617",
    relief="flat"
)
jetzt = datetime.now()
stunden_spin.delete(0, "end")
stunden_spin.insert(0, f"{jetzt.hour:02d}")
stunden_spin.grid(row=0, column=1, padx=5)

# Label für Minuten
tk.Label(
    eingabe_frame,
    text="",
    font=("Segoe UI", 11),
    fg="#38bdf8",
    bg="#0f172a"
).grid(row=0, column=2, padx=5)

# Spinbox für Minuten (0-59)
minuten_spin = tk.Spinbox(
    eingabe_frame,
    from_=0,
    to=59,
    width=4,
    font=("Consolas", 14),
    justify="center",
    bg="#020617",
    fg="#e5e7eb",
    buttonbackground="#020617",
    relief="flat"
)
minuten_spin.delete(0, "end")
minuten_spin.insert(0, f"{jetzt.minute:02d}")
minuten_spin.grid(row=0, column=3, padx=5)

# Styling für Combobox
style = ttk.Style()
style.theme_use('clam')
style.configure('TCombobox', fieldbackground="#020617", foreground="#e5e7eb", background="#C0C2C9")

# Enter-Taste bindet zur Berechnung
stunden_spin.bind("<Return>", lambda event: berechne_feierabend())
minuten_spin.bind("<Return>", lambda event: berechne_feierabend())

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
