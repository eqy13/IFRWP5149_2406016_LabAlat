| Elemen SIA-RO1 — Lihat Jadwal Kuliah| |
| :--- | :--- |
| Elemen | SIA-RO1 — Lihat jadwal kuliah |
| Tujuan | Menampilkan informasi jadwal kuliah yang aktif kepada mahasiswa. |
| Aktor Utama | Mahasiswa |
| Sumber Kebutuhan| SIA-R01 |
| Pemicu | Mahasiswa memilih fungsi lihat/cetak jadwal kuliah pada menu utama. |
| Prasyarat | Mahasiswa telah terautentikasi; data jadwal kuliah telah diisi oleh admin. |
| Pascakondisi Berhasil| Jadwal kuliah berhasil ditampilkan pada layar mahasiswa. |
| Pascakondisi Gagal | Sistem menampilkan pesan bahwa jadwal belum tersedia atau gagal dimuat. |


| Elemen SIA-RO2 — Kelola jadwal kuliah| |
| :--- | :--- |
| Elemen | SIA-RO2 — Kelola jadwal kuliah |
| Tujuan | Menambah, mengubah, atau menghapus data jadwal kuliah di dalam sistem. |
| Aktor Utama | Admin akademik |
| Sumber Kebutuhan| SIA-R02 |
| Pemicu | Admin mengakses menu manajemen atau pengelolaan jadwal kuliah. |
| Prasyarat | Admin telah terautentikasi dan memiliki hak akses manajerial jadwal. |
| Pascakondisi Berhasil| Perubahan data jadwal kuliah (tambah/edit/hapus) berhasil disimpan ke dalam basis data. |
| Pascakondisi Gagal | Data jadwal lama tidak berubah; sistem menampilkan pesan kesalahan input atau kegagalan sistem. |


|  Elemen SIA-RO3 — Ajukan KRS  |  |
| :--- | :--- |
| Elemen | SIA-RO3 --> Mengajukan KRS |
| Tujuan | Menghasilkan draf rencana studi mahasiswa yang diajukan ke dosen wali. | 
| Aktor Utama | Mahasiswa | 
| Sumber Kebutuhan | SIA-R03, SIA-R04, dan SIA-R05 |
| Pemicu | Mahasiswa memilih fungsi pengajuan KRS pada menu utama. | 
| Prasyarat | Mahasiswa telah terautentikasi; masa pengisian KRS sedang aktif; data mata kuliah tersedia. | 
| Pascakondisi diterima | Pengajuan KRS tersimpan ke basis data dengan status Menunggu keputusan. | 
| Pascakondisi ditolak | Tidak ada pengajuan baru yang berhasil tersimpan; mahasiswa diminta memperbaiki pilihan mata kuliah. | 
| Include | SIA-RO4 --> Memvalidasi KRS | 
| Extension point | Bukti pengajuan tersedia, pada konfirmasi pengajuan |
| Extend | SIA-UC05 — Unduh bukti pengajuan jika [mahasiswa memilih unduh bukti pada konfirmasi pengajuan] | 


|  Elemen SIA-RO4 — Validasi KRS |  |
| :--- | :--- |
| Elemen | SIA-RO4 --> Validasi KRS |
| Tujuan | Memastikan mata kuliah yang diambil mahasiswa memenuhi aturan akademik (tidak bentrok jadwal, prasyarat terpenuhi, dan tidak melebihi kuota SKS). | 
| Aktor Utama | Sistem | 
| Sumber Kebutuhan | SIA-RO4 |
| Pemicu | Dipanggil secara otomatis oleh SIA-UC03 — Ajukan KRS sebelum konfirmasi akhir. | 
| Prasyarat | Data draf mata kuliah yang dipilih oleh mahasiswa sudah diterima oleh sistem. | 
| Pascakondisi diterima | Validasi lolos; sistem mengizinkan proses pengajuan KRS berlanjut ke tahap konfirmasi. | 
| Pascakondisi ditolak | Validasi gagal; sistem menghentikan proses pengajuan KRS dan mengembalikan daftar kesalahan validasi ke layar mahasiswa. | 
| Include | - | 
| Extension point | - |
| Extend | - | 


|  Elemen SIA-UC05 —  Unduh bukti pengajuan  |  |
| :--- | :--- |
| Elemen | SIA-RO5 --> Unduh bukti pengajuan |
| Tujuan | Menghasilkan dokumen digital (PDF) sebagai bukti fisik pengajuan KRS yang sah. | 
| Aktor Utama | Mahasiswa | 
| Sumber Kebutuhan | SIA-RO5 |
| Pemicu | Dipicu dari extension point pada SIA-UC03 — Ajukan KRS. | 
| Prasyarat | Mahasiswa mencentang opsi unduh bukti saat melakukan konfirmasi pengajuan KRS. | 
| Pascakondisi diterima | Dokumen bukti pengajuan KRS berhasil diunduh ke perangkat mahasiswa. | 
| Pascakondisi ditolak | Dokumen gagal diunduh; sistem memberikan opsi untuk mengunduh ulang melalui riwayat pengajuan. | 
| Include | - | 
| Extension point | - |
| Extend | - |


|  Elemen SIA-UC06 —  Proses persetujuan KRS  |  |
| :--- | :--- |
| Elemen | SIA-RO5 --> Proses persetujuan KRS |
| Tujuan | Menghasilkan keputusan akhir (setuju/tolak) beserta catatan keputusan atas rencana studi yang diajukan mahasiswa bimbingan. | 
| Aktor Utama | Dosen Wali | 
| Sumber Kebutuhan | SIA-RO6 |
| Pemicu | Dosen wali memilih fungsi perwalian atau daftar antrean KRS mahasiswa. | 
| Prasyarat | Dosen wali telah terautentikasi; terdapat data mahasiswa bimbingan dengan status KRS Menunggu keputusan. | 
| Pascakondisi diterima | Status pengajuan KRS mahasiswa berubah menjadi Disetujui atau Ditolak, dan catatan keputusan dari dosen wali berhasil tersimpan ke dalam sistem. | 
| Pascakondisi ditolak | Status pengajuan KRS mahasiswa tidak berubah (tetap Menunggu keputusan) dan catatan keputusan tidak tersimpan. | 
| Include | - | 
| Extension point | - |
| Extend | - |