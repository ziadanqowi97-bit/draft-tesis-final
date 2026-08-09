# Draft Tesis - LaTeX

Repositori ini berisi draf penulisan tesis magister/doktor menggunakan sistem typesetting **LaTeX**. Struktur repositori ini dioptimalkan untuk memisahkan setiap bab dan mengelola sitasi secara modular.

## 📂 Struktur Repositori

```text
├── main.tex             # File utama untuk kompilasi dokumen
├── references.bib       # Database bibliografi/daftar pustaka (BibTeX)
├── metadata.tex         # Informasi judul, nama penulis, NIM/NRP, dan dosen pembimbing
├── chapters/            # Folder berisi konten utama tesis per bab
│   ├── bab1.tex         # Pendahuluan
│   ├── bab2.tex         # Tinjauan Pustaka
│   ├── bab3.tex         # Metodologi Penelitian
│   ├── bab4.tex         # Hasil dan Pembahasan
│   └── bab5.tex         # Kesimpulan dan Saran
├── figures/             # Menyimpan semua file gambar dan ilustrasi
└── README.md            # Dokumentasi repositori ini
```

## 🛠️ Prasyarat & Lingkungan Kerja

Untuk mengompilasi dan mengedit draf tesis ini, Anda memerlukan komponen berikut:

1. **Distribusi LaTeX:**
   * **Windows:** [MiKTeX](https://miktex.org) atau [TeX Live](https://tug.org)
   * **Linux (Ubuntu/Debian):** `sudo apt install texlive-full`
   * **macOS:** [MacTeX](https://tug.org)
2. **Editor Teks:**
   * [VS Code](https://visualstudio.com) dengan ekstensi **LaTeX Workshop** (Sangat Direkomendasikan).
   * Alternatif: [Overleaf](https://overleaf.com) (Unggah seluruh folder sebagai proyek baru), TeXstudio, atau TeXworks.
3. **Compiler Engine:** Proyek ini menggunakan `pdflatex` atau `latexmk` untuk proses kompilasi otomatis.

## 🚀 Cara Menjalankan & Mengompilasi

### Menggunakan VS Code (Lokal)
1. Clone repositori ini ke komputer Anda.
2. Buka folder proyek menggunakan VS Code.
3. Buka file `main.tex`.
4. Jika ekstensi **LaTeX Workshop** sudah terpasang, tekan tombol **Build LaTeX Project** pada bilah menu samping (ikon TeX) atau tekan shortcut `Ctrl + Alt + B`.
5. Hasil dokumen akhir berformat PDF akan otomatis ter-generate di folder utama (`main.pdf`).

### Menggunakan Terminal / Command Line
Jika Anda menggunakan `latexmk`, jalankan perintah berikut pada direktori root proyek:
```bash
latexmk -pdf main.tex
```

## 📝 Catatan Penulisan
* Jangan menulis teks langsung di dalam `main.tex`. Selalu buat file `.tex` baru di dalam folder `chapters/` jika ingin menambah sub-bagian, lalu panggil menggunakan perintah `\input{chapters/nama_file}` di dalam `main.tex`.
* Untuk sitasi, pastikan data referensi telah dimasukkan ke file `references.bib` dengan format BibTeX, lalu panggil menggunakan sintaks `\cite{citation_key}` di dalam tulisan.

## 🧑‍💻 Penulis
* **Nama:** Ziadan Qowi
* **NIM/NRP:** 23524019
* **Program Studi:** Magister Informatika
* **Institusi:** Institut Teknologi Bandung
