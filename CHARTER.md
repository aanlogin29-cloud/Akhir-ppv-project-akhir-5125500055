# Project Charter: KostBudget (Aplikasi Pengelolaan Keuangan Kos Mahasiswa)

## 1. Pernyataan Masalah
Mahasiswa perantauan sering mengalami kesulitan dalam memantau pengeluaran harian dan bulanan secara transparan. Pencatatan manual sering kali tidak praktis dan menyebabkan mahasiswa kehabisan anggaran sebelum akhir bulan.

## 2. Pengguna Sasaran (Persona)
* **Nama:** Rian (Mahasiswa Perantauan)
* **Keseharian:** Kuliah dari pagi sampai sore, mengandalkan uang bulanan yang terbatas, sering membeli makanan luar dan kebutuhan mendadak.
* **Masalah:** Sering lupa mencatat pengeluaran kecil harian yang berakibat defisit keuangan di minggu ketiga.

## 3. Fitur MVP (MoSCoW Prioritization)
* **Must Have:**
  1. Input transaksi pemasukan dan pengeluaran harian (Nominal, Kategori, Keterangan).
  2. Ringkasan saldo total secara real-time (Pemasukan, Pengeluaran, Sisa Saldo).
  3. Daftar riwayat transaksi dengan opsi hapus data.
* **Should Have:**
  1. Filter riwayat transaksi berdasarkan kategori.
* **Could Have:**
  1. Indikator visual peringatan jika pengeluaran mendekati batas anggaran.
* **Won't Have (Sengaja Tidak Dibuat di Sprint Ini):**
  1. Fitur ekspor laporan ke PDF/Excel (ditunda ke proyek lanjutan).

## 4. Kriteria Sukses Terukur
* Pengguna baru dapat mencatat transaksi pertama dalam waktu **≤ 2 menit** tanpa bantuan manual.
* Antarmuka responsif dan mulus diakses melalui ponsel (lebar layar ± 400 px) maupun laptop.

## 5. Risiko dan Antisipasi
1. **Risiko:** Data transaksi hilang saat peramban ditutup.
   * **Antisipasi:** Menggunakan penyimpanan lokal (`localStorage`) pada sisi klien.
2. **Risiko:** Tampilan layout rusak di layar ponsel kecil.
   * **Antisipasi:** Menerapkan sistem grid dan komponen responsif dari Bootstrap.
3. **Risiko:** Kesalahan input angka kosong oleh pengguna.
   * **Antisipasi:** Validasi formulir HTML5 (`required`).