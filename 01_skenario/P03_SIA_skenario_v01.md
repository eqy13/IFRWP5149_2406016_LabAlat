```text
Mahasiswa mengajukan KRS dengan memilih mata kuliah. Setiap
pengajuan menjalankan validasi KRS yang memeriksa kelengkapan,
prasyarat mata kuliah, dan benturan jadwal. Jika validasi berhasil,
sistem menyimpan pengajuan berstatus menunggu persetujuan dosen
wali. Pada konfirmasi penyimpanan, mahasiswa dapat memilih
mengunduh bukti pengajuan. Dosen wali menyetujui atau menolak KRS
dan memberikan catatan keputusan.
```

| **ID** | **Kebutuhan** |
| :--- | :--- | 
| **SIA-R01** | Mahasiswa dapat melihat jadwal kuliah | 
| **SIA-R02** | Admin akademik dapat mengelola jadwal kuliah | 
| **SIA-R03** | Mahasiswa dapat mengajukan KRS |
| **SIA-R04** | Sistem memvalidasi KRS sebagai bagian pengajuan |
| **SIA-R05** | Mahasiswa dapat mengunduh bukti jika memilihnya pada konfirmasi pengajuan |
| **SIA-RO6** | Dosen wali dapat memproses persetujuan atau penolakan KRS |

```text
Batas dan asumsi:
• Pengguna telah terautentikasi.
• Data mata kuliah, prasyarat, dan jadwal tersedia.
• Validasi gagal menyebabkan pengajuan belum berhasil tersimpan.
• Unduh bukti tidak menjadi syarat keberhasilan pengajuan.
• KRS tersimpan belum berarti disetujui.
• Pembayaran, pengisian nilai, dan implementasi basis data berada di luar tugas.
```


|  Elemen SIA-RO3 — Ajukan KRS  |  |
| :--- | :--- |
| Elemen | SIA-RO3 --> Mengajukan KRS |
| Tujuan | Menghasilkan pengajuan KRS yang disimpan | 
| Aktor Utama | Mahasiswa | 
| Sumber Kebutuhan | SIA-RO3 dan SIA-RO4 |
| Pemicu | Mahasiswa memilih fungsi pengajuan KRS | 
| Prasyarat | Mahasiswa telah terautentikasi; data mata kuliah, prasyarat, dan jadwal tersedia | 
| Pascakondisi diterima | Pengajuan tersimpan dengan status menunggu persertujuan dosen wali | 
| Pascakondisi ditolak | Tidak ada pengajuan baru yang disimpan | 
| Include | SIA-RO4 --> Memvalidasi KRS | 
| Extension point | Konfirmasi penyimpanan tersedia, pada langkah 6 |
| Extend | SIA-UC03 jika [mahasiswa memilih mengunduh bukti] | 

|  Elemen SIA-UC04 — Memproses Pengajuan |  |
| :--- | :--- |
| Elemen | SIA-RO4 --> Mengajukan KRS |
| Tujuan | Menghasilkan status keputusan KRS yang diperbarui beserta catatan | 
| Aktor Utama | Dosen Wali | 
| Sumber Kebutuhan | SIA-RO6 |
| Pemicu | Dosen Wali memilih fungsi proses keputusan KRS | 
| Prasyarat | Dosen Wali telah terautentikasi; data pengajuan KRS berstatus menunggu persetujuan tersedia | 
| Pascakondisi diterima | Status KRS diperbarui (Disetujui/Ditolak) dan catatan keputusan tersimpan | 
| Pascakondisi ditolak | Status KRS tidak mengalami perubahan | 
| Include | - | 
| Extension point | - |
| Extend | - | 


