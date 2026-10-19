<!-- Skenario -->
```text
Skenario tugas berikut fiktif untuk praktikum dan berbeda dari tugas
Pertemuan 2 (jadwal kuliah) dan Pertemuan 3 (pengajuan KRS).
Mahasiswa dan dosen sama-sama merupakan Civitas Akademika yang
dapat melihat kalender akademik. Dosen menginput nilai mata kuliah yang
diampunya setelah masa perkuliahan berakhir. Mahasiswa melihat Kartu
Hasil Studi (KHS) untuk semester yang nilainya sudah dipublikasikan. Admin
Akademik mengelola data mahasiswa: menambah data mahasiswa baru,
mengubah data mahasiswa, dan menghapus data mahasiswa. Dua use case
utama, Input Nilai Mata Kuliah dan Lihat KHS, ditunjukkan realisasinya oleh
collaboration yang bersesuaian.
```

<!-- Batas dan Asumsi -->
```text
Batas dan asumsi
• Kode kebutuhan dimulai dari SIA-R07 agar SIA-R01 dan SIA-R02
(Pertemuan 2) serta SIA-R03 sampai SIA-R06 (Pertemuan 3) tetap
mempunyai identitas berbeda.
• Pengguna telah terautentikasi dan memiliki hak akses sesuai peran.
• Kalender akademik pada tugas ini adalah agenda resmi institusi (awal
semester, batas KRS, masa ujian, dan sejenisnya); jangan
menyamakannya dengan jadwal kuliah pada Pertemuan 2.
• Nilai hanya dapat diinput oleh dosen pengampu mata kuliah tersebut. Nilai
yang diinput belum terpublikasi sebelum dinyatakan resmi oleh ketentuan
tugas ini: KHS hanya menampilkan nilai yang sudah dipublikasikan.
• Hapus Data Mahasiswa hanya untuk mahasiswa yang tidak memiliki data
akademik aktif. Ketentuan ini fiktif untuk latihan.
• Pengajuan KRS tetap digambar sebagai bagian diagram kumulatif dari
Pertemuan 3. Pembayaran dan perancangan basis data berada di luar
tugas ini.
```

<!-- Aktor dan Use Case -->
| ID Use Case | Nama Use Case | Aktor Terkait | Sumber Kebutuhan | Status |
| :--- | :--- | :--- | :--- | :--- |
| **SIA-UC01** | Lihat Jadwal Kuliah | Mahasiswa / Dosen | Pertemuan 2 | Tetap |
| **SIA-UC02** | Kelola Jadwal Kuliah | Admin Akademik | Pertemuan 2 | Tetap |
| **SIA-UC03** | Ajukan KRS | Mahasiswa | Pertemuan 3 | Tetap |
| **SIA-UC04** | Validasi KRS | Dosen Wali | Pertemuan 3 | Tetap |
| **SIA-UC05** | Unduh Bukti Pengajuan KRS | Mahasiswa | Pertemuan 3 | Tetap |
| **SIA-UC06** | Proses Keputusan KRS | Admin Akademik / Dosen Wali | Pertemuan 3 | Tetap |
| **SIA-UC07** | Lihat Kalender Akademik | Civitas Akademika (Mahasiswa & Dosen) | SIA-R07 | Baru |
| **SIA-UC08** | Input Nilai Mata Kuliah | Dosen | SIA-R08 | Baru |
| **SIA-UC09** | Lihat KHS | Mahasiswa | SIA-R09 | Baru |
| **SIA-UC10** | Kelola Data Mahasiswa *(General)* | Admin Akademik | SIA-R10 | Baru |
| **SIA-UC11** | Tambah Data Mahasiswa *(Spesifik)* | Admin Akademik | SIA-R11 | Baru |
| **SIA-UC12** | Ubah Data Mahasiswa *(Spesifik)* | Admin Akademik | SIA-R11 | Baru |
| **SIA-UC13** | Hapus Data Mahasiswa *(Spesifik)* | Admin Akademik | SIA-R11 | Baru |
