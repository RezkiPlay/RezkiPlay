import tkinter as tk
from tkinter import messagebox
from tkinter import font

# Fungsi untuk menghitung winrate
def hitung_winrate():
    try:
        # Ambil input dari user dan konversi menjadi integer
        kemenangan = int(entry_kemenangan.get())
        total_pertandingan = int(entry_total_pertandingan.get())

        # Validasi jika total pertandingan nol
        if total_pertandingan == 0:
            messagebox.showerror("Error", "Total pertandingan tidak boleh nol!")
        else:
            # Hitung winrate dan tampilkan hasilnya
            winrate = (kemenangan / total_pertandingan) * 100
            label_hasil.config(text=f"Winrate: {round(winrate, 2)}%")
    
    except ValueError:
        # Tampilkan pesan error jika input bukan angka
        messagebox.showerror("Error", "Masukkan nilai numerik yang valid!")

# Membuat jendela utama
root = tk.Tk()
root.title("Penghitung Winrate")
root.geometry("400x300")  # Mengatur ukuran jendela

# Menambahkan warna latar belakang
root.configure(bg="#282a36")

# Menambahkan font khusus
judul_font = font.Font(family="Helvetica", size=16, weight="bold")
label_font = font.Font(family="Arial", size=12)
hasil_font = font.Font(family="Arial", size=14, weight="bold")

# Label judul aplikasi
label_judul = tk.Label(root, text="Aplikasi Penghitung Winrate", font=judul_font, fg="#f8f8f2", bg="#282a36")
label_judul.grid(row=0, column=0, columnspan=2, pady=10)

# Label dan entri untuk jumlah kemenangan
label_kemenangan = tk.Label(root, text="Jumlah Kemenangan:", font=label_font, fg="#f8f8f2", bg="#282a36")
label_kemenangan.grid(row=1, column=0, padx=10, pady=10, sticky="w")
entry_kemenangan = tk.Entry(root, width=15)
entry_kemenangan.grid(row=1, column=1, padx=10, pady=10)

# Label dan entri untuk total pertandingan
label_total_pertandingan = tk.Label(root, text="Total Pertandingan:", font=label_font, fg="#f8f8f2", bg="#282a36")
label_total_pertandingan.grid(row=2, column=0, padx=10, pady=10, sticky="w")
entry_total_pertandingan = tk.Entry(root, width=15)
entry_total_pertandingan.grid(row=2, column=1, padx=10, pady=10)

# Tombol untuk menghitung winrate
button_hitung = tk.Button(root, text="Hitung Winrate", font=label_font, bg="#6272a4", fg="#f8f8f2", command=hitung_winrate)
button_hitung.grid(row=3, column=0, columnspan=2, pady=20)

# Label untuk menampilkan hasil winrate
label_hasil = tk.Label(root, text="Winrate: ", font=hasil_font, fg="#50fa7b", bg="#282a36")
label_hasil.grid(row=4, column=0, columnspan=2, pady=10)

# Menjalankan aplikasi
root.mainloop()
