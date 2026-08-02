# 📅 Schedule Maker

Aplikasi desktop berbasis Java Swing untuk mengelola jadwal kuliah dan kegiatan harian secara praktis dalam satu dashboard.

## ✨ Fitur

- **Tambah, Edit, dan Hapus Jadwal** — kelola semua aktivitas dari satu tabel interaktif.
- **Klasifikasi Kegiatan** — bedakan antara **Kuliah** dan **Kegiatan Harian**.
- **Skala Prioritas (1–5)** — urutkan kegiatan berdasarkan tingkat prioritas secara otomatis.
- **Sorting Otomatis** — tabel jadwal terurut berdasarkan prioritas tertinggi.
- **Validasi Input** — memastikan data wajib (nama, hari, prioritas) terisi sebelum disimpan.
- **Reset Cepat** — hapus seluruh jadwal dan form dengan satu klik.
- **Tampilan Modern** — desain UI terinspirasi dari palet warna ala Tailwind CSS.

## 🖥️ Tampilan Aplikasi

Dashboard terdiri dari dua bagian utama:
1. **Sidebar Form** (kiri) — input data kegiatan seperti nama, jenis, hari, waktu, prioritas, dan deskripsi.
2. **Tabel Jadwal** (kanan) — menampilkan seluruh kegiatan yang telah ditambahkan, lengkap dengan aksi Tambah, Edit, Hapus, Reset, dan Keluar.

## 🏗️ Struktur Proyek

```
Schedule_Maker/
├── src/
│   ├── Main.java                 # Entry point aplikasi
│   ├── ScheduleMakerApp.java     # Entry point alternatif
│   ├── ScheduleMakerGUI.java     # Tampilan utama (GUI Swing)
│   ├── AbstractKegiatan.java     # Kelas abstrak dasar kegiatan
│   ├── Kegiatan.java             # Kegiatan umum (turunan AbstractKegiatan)
│   ├── Kuliah.java                # Kegiatan kuliah (turunan Kegiatan)
│   ├── KegiatanHarian.java       # Kegiatan harian (turunan Kegiatan)
│   ├── Jadwal.java                # Pengelola daftar kegiatan
│   └── User.java                  # Pengelola daftar jadwal milik pengguna
├── .idea/                         # Konfigurasi IntelliJ IDEA
└── .gitignore
```

## 🧩 Konsep OOP yang Digunakan

- **Abstraction** — `AbstractKegiatan` sebagai kelas dasar abstrak.
- **Inheritance** — `Kegiatan` mewarisi `AbstractKegiatan`; `Kuliah` dan `KegiatanHarian` mewarisi `Kegiatan`.
- **Polymorphism** — method `tampilkanDetail()` dan `getTipeKegiatan()` di-override sesuai jenis kegiatan.
- **Encapsulation** — seluruh atribut kelas bersifat private dengan getter/setter.

## 🚀 Cara Menjalankan

### Menggunakan IntelliJ IDEA / IDE Java lainnya
1. Clone repository ini:
   ```bash
   git clone https://github.com/Rizkydi2/Schedule_Maker.git
   ```
2. Buka project di IDE (IntelliJ IDEA direkomendasikan, karena sudah tersedia konfigurasi `.idea/`).
3. Jalankan file `Main.java` atau `ScheduleMakerApp.java`.

### Menggunakan terminal
```bash
cd src
javac *.java
java src.Main
```

## 🛠️ Teknologi

- **Java** (Java Swing untuk GUI)
- **IntelliJ IDEA** sebagai IDE pengembangan

## 👥 Kontributor

- Rizkydi2
- Shakyawanbaguswijaya

## 📄 Lisensi

Proyek ini dibuat untuk keperluan tugas kuliah.
