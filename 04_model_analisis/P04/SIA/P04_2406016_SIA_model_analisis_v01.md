| Sumber | Hubungan / Tipe | Tujuan |
| :--- | :--- | :--- |
| **Civitas Akademika** | Association | SIA-UC07 Lihat Kalender Akademik |
| **Mahasiswa** | Association *(tetap dari Pertemuan 2)* | SIA-UC01 Lihat Jadwal Kuliah |
| **Mahasiswa** | Association *(tetap dari Pertemuan 3)* | SIA-UC03 Ajukan KRS |
| **Mahasiswa** | Association *(khusus, tetap dari Pertemuan 3)* | SIA-UC05 Unduh Bukti Pengajuan KRS |
| **Mahasiswa** | Association | SIA-UC09 Lihat KHS |
| **Mahasiswa** | Generalization `→` | Civitas Akademika |
| **Dosen** | Association *(tetap dari Pertemuan 2)* | SIA-UC01 Lihat Jadwal Kuliah |
| **Dosen** | Association | SIA-UC08 Input Nilai Mata Kuliah |
| **Dosen** | Generalization `→` | Civitas Akademika |
| **Dosen Wali** | Association *(tetap dari Pertemuan 3)* | SIA-UC04 Validasi KRS |
| **Dosen Wali** | Association *(tetap dari Pertemuan 3)* | SIA-UC06 Proses Keputusan KRS |
| **Admin Academic** | Association *(tetap dari Pertemuan 2)* | SIA-UC02 Kelola Jadwal Kuliah |
| **Admin Academic** | Association *(tetap dari Pertemuan 3)* | SIA-UC06 Proses Keputusan KRS |
| **Admin Academic** | Association | SIA-UC10 Kelola Data Mahasiswa |
| **SIA-UC03 Ajukan KRS** | `«include»` *(tetap dari Pertemuan 3)* | SIA-UC04 Validasi KRS |
| **SIA-UC05 Unduh Bukti Pengajuan KRS** | `«extend»` *(tetap dari Pertemuan 3)* | SIA-UC03 Ajukan KRS |
| **SIA-UC11 Tambah Data Mahasiswa** | Generalization `→` | SIA-UC10 Kelola Data Mahasiswa |
| **SIA-UC12 Ubah Data Mahasiswa** | Generalization `→` | SIA-UC10 Kelola Data Mahasiswa |
| **SIA-UC13 Hapus Data Mahasiswa** | Generalization `→` | SIA-UC10 Kelola Data Mahasiswa |
| **SIA-CO01 (collaboration)** | Realization `→` | SIA-UC08 Input Nilai Mata Kuliah |
| **SIA-CO02 (collaboration)** | Realization `→` | SIA-UC09 Lihat KHS |
