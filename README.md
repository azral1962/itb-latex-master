# Quarto ITB Thesis

Extension dan starter project Quarto Book untuk menulis dokumen ilmiah ITB
(Tugas Akhir, Tesis, atau Disertasi) dan menghasilkan PDF melalui LaTeX.

## Mulai cepat

1. Ubah metadata dokumen pada `_quarto.yml`.
2. Tulis isi dokumen pada `index.qmd`, `chapters/`, dan `appendices/`.
3. Render dokumen:

   ```powershell
   quarto render
   ```

Hasil PDF berada di `_book/dokumen-itb.pdf`. Opsi `keep-tex: true` pada
extension juga mempertahankan sumber `dokumen-itb.tex` di direktori proyek.

Proyek memerlukan Quarto serta distribusi LaTeX seperti TeX Live atau MiKTeX.

## Struktur

- `_extensions/itb-thesis/` — project type dan format PDF extension.
- `_quarto.yml` — metadata mahasiswa, program studi, pembimbing, dan urutan bab.
- `index.qmd` — Bab I.
- `chapters/` — Bab II sampai Bab V serta daftar pustaka.
- `appendices/` — lampiran.
- `resources/` — gambar dan data yang digunakan di dalam bab.
- `references.bib` — basis data referensi.
- `if-itb-latex-master/` — templat LaTeX sumber yang dipertahankan sebagai
  referensi historis.

## Menggunakan sebagai template

Setelah repositori dipublikasikan ke GitHub, pengguna dapat membuat proyek baru
dengan:

```bash
quarto use template ORGANISASI/NAMA-REPOSITORI
```

Untuk memasang formatnya saja ke proyek Quarto yang sudah ada:

```bash
quarto add ORGANISASI/NAMA-REPOSITORI
```

Format dapat dipilih secara eksplisit dengan `itb-thesis-pdf`.

## Metadata halaman awal

Seluruh data yang biasanya tersebar pada beberapa berkas LaTeX tersedia di
`_quarto.yml`, antara lain:

- `book.title`, `book.author`, dan `student-id`;
- `document-type`, `degree`, `study-program`, `school`, dan `university`;
- `cover-date`, `approval-date`, dan `statement-date`;
- daftar `supervisors` beserta peran dan NIP;
- `abstract-id`, `abstract-en`, daftar kata kunci, dan `acknowledgements`.

Jenis dokumen dapat diubah menjadi Tugas Akhir, Tesis, atau Disertasi cukup
dengan mengganti metadata tersebut tanpa menyunting partial LaTeX.
