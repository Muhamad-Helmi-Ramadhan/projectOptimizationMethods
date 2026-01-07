# Smart Budgeting dengan Branch and Bound

## Apa itu Branch and Bound?

**Branch and Bound** adalah algoritma optimasi yang digunakan untuk **memilih kombinasi terbaik dari banyak pilihan** tanpa melebihi batas tertentu (misal budget).  

Prinsip kerjanya:
- **Branch (Cabang)** → setiap item bisa dipilih atau tidak dipilih, sehingga tercipta banyak kombinasi.
- **Bound (Batas)** → hitung nilai maksimum yang mungkin dari setiap cabang. Cabang yang **tidak mungkin lebih baik** akan dipangkas agar algoritma lebih efisien.  

Dalam proyek ini:
- Digunakan untuk memilih **item prioritas** agar **total nilai (prioritas) maksimal** dengan batas budget tertentu.  
- **Konsumsi wajib masuk** jika budget mencukupi (≥ 2 juta).

---

## Isi Excel (`Branch and Bound.xlsx`)

Excel digunakan sebagai **awal perhitungan sebelum membuat program**. Fungsinya:

1. **Daftar Item**: Nama item, biaya (`cost`), dan prioritas (`value`).
2. **Rasio Efisiensi**: Kolom `value / cost` untuk menentukan item mana yang lebih “efisien” jika dibandingkan biaya.
3. **Simulasi Kombinasi**:
   - Menghitung total biaya dan total nilai dari beberapa kombinasi item.
   - Menandai kombinasi yang **melebihi budget**.
   - Menentukan kombinasi dengan **nilai total maksimal** sesuai batas budget.
4. Hasil Excel ini kemudian diterjemahkan ke dalam **Python/HTML**, sehingga program bisa menghitung otomatis kombinasi optimal.

> Intinya: Excel membantu **memvisualisasi logika Branch and Bound** sebelum diubah menjadi kode program.

---

## Struktur File

| File | Deskripsi |
|------|-----------|
| `Branch and Bound.xlsx` | Perhitungan awal di Excel, simulasi kombinasi item |
| `program1.py` | Python Branch and Bound (bisa dijalankan di Google Colab) |
| `index.html` | UI interaktif dengan Capybara |
| `capybara.png` | Maskot Capybara untuk tampilan HTML |
| `README.md` | Dokumentasi proyek |

---

## Cara Menjalankan Python (`program1.py`)

1. Buka **Google Colab** atau lokal Python.
2. Upload `program1.py`.
3. Jalankan script dan atur `budget`.
4. Output menampilkan:
   - Item yang dipilih
   - Total biaya
   - Total prioritas

---

## Cara Menjalankan Program HTML (`index.html`)

1. Buka file `index.html` di browser.
2. Masukkan budget.
3. Tambahkan item prioritas baru jika perlu.
4. Klik **Analisis Alokasi** untuk melihat hasil interaktif.

---

## Catatan

- Program fleksibel: bisa ubah nilai prioritas, biaya, dan budget.  
- Cocok untuk belajar optimasi sederhana dan budgeting interaktif.
