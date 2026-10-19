| Elemen | Deskripsi |
| :--- | :--- |
| **ID dan Nama** | SIA-UC07: Lihat Kalender Akademik |
| **Sumber Kebutuhan** | SIA-R07 |
| **Tujuan** | Menampilkan informasi jadwal kegiatan akademik kampus dalam satu periode |
| **Aktor Utama** | Civitas Akademika (Mahasiswa dan Dosen) |
| **Pemicu** | Pengguna memilih menu Kalender Akademik |
| **Prasyarat** | Pengguna telah masuk ke dalam sistem |
| **Pascakondisi Berhasil** | Sistem berhasil menampilkan kalender akademik yang aktif saat ini |
| **Pascakondisi Gagal** | Sistem menampilkan pesan kesalahan gagal memuat data |
| **Include** | - |
| **Collaboration** | - |


| Elemen | Deskripsi |
| :--- | :--- |
| **ID dan Nama** | SIA-UC08: Input Nilai Mata Kuliah |
| **Sumber Kebutuhan** | SIA-R08 |
| **Tujuan** | Menyimpan nilai mahasiswa untuk mata kuliah tertentu ke dalam sistem |
| **Aktor Utama** | Dosen |
| **Pemicu** | Dosen memilih fungsi input nilai mata kuliah |
| **Prasyarat** | Dosen telah terautentikasi; Dosen adalah pengampu sah dari mata kuliah yang dipilih |
| **Alur Utama (Basic Flow)** | 1. Dosen memilih kelas dan mata kuliah yang diampu.<br>2. Sistem menampilkan daftar mahasiswa.<br>3. Dosen memasukkan nilai (angka/huruf) untuk setiap mahasiswa.<br>4. Dosen menekan tombol simpan.<br>5. Sistem memvalidasi rentang nilai.<br>6. Sistem menyimpan nilai dan memperbarui status nilai. |
| **Alur Alternatif (Alt Flow)** | **[Nilai di Luar Rentang]** Pada langkah 5, jika dosen memasukkan nilai di luar rentang yang sah (misal: < 0 atau > 100), sistem akan menampilkan pesan eror, menolak input tersebut, dan meminta dosen memasukkan kembali nilai yang valid. |
| **Pascakondisi Berhasil** | Nilai mahasiswa berhasil tersimpan di dalam sistem dengan status draf/final |
| **Pascakondisi Gagal** | Tidak ada nilai baru yang tersimpan atau diperbarui; data nilai kembali ke kondisi semula |
| **Include** | - |
| **Collaboration** | SIA-CO01: Input Nilai Mata Kuliah (SIA-R12) |


| Elemen | Deskripsi |
| :--- | :--- |
| **ID dan Nama** | SIA-UC09: Lihat KHS (Kartu Hasil Studi) |
| **Sumber Kebutuhan** | SIA-R09 |
| **Tujuan** | Menampilkan rangkuman nilai studi mahasiswa pada semester tertentu, di mana hanya nilai yang sudah dipublikasikan yang ditampilkan |
| **Aktor Utama** | Mahasiswa |
| **Pemicu** | Mahasiswa memilih menu Kartu Hasil Studi (KHS) dan memilih semester |
| **Prasyarat** | Mahasiswa telah terautentikasi; Data nilai semester terpilih sudah tersedia |
| **Pascakondisi Berhasil** | Sistem berhasil menampilkan lembar KHS yang memuat nilai-nilai yang berstatus telah dipublikasikan |
| **Pascakondisi Gagal** | Nilai belum dirilis atau sistem gagal memuat halaman KHS |
| **Include** | - |
| **Collaboration** | SIA-CO02: Lihat KHS (SIA-R12) |


| Elemen | Deskripsi |
| :--- | :--- |
| **ID dan Nama** | SIA-UC10: Kelola Data Mahasiswa |
| **Sumber Kebutuhan** | SIA-R10 |
| **Tujuan** | Menjadi use case umum/induk untuk manajemen data identitas dan status mahasiswa |
| **Aktor Utama** | Admin Akademik |
| **Pemicu** | Admin masuk ke dasbor manajemen mahasiswa |
| **Prasyarat** | Admin telah terautentikasi dan memiliki hak akses manajemen data |
| **Pascakondisi Berhasil** | Menu manajemen mahasiswa terbuka dan siap menerima aksi turunan |
| **Pascakondisi Gagal** | Akses ditolak atau sistem gagal menampilkan daftar mahasiswa |
| **Include** | - |
| **Collaboration** | - |


| Elemen | Deskripsi |
| :--- | :--- |
| **ID dan Nama** | SIA-UC11: Tambah Data Mahasiswa |
| **Sumber Kebutuhan** | SIA-R11 |
| **Tujuan** | Mendaftarkan mahasiswa baru ke dalam database sistem |
| **Aktor Utama** | Admin Akademik |
| **Pemicu** | Admin memilih tombol "Tambah Mahasiswa" pada menu kelola data |
| **Prasyarat** | Admin telah berada di halaman SIA-UC10; Formulir data mahasiswa baru siap diisi |
| **Pascakondisi Berhasil** | Data mahasiswa baru tersimpan di database dan akun mahasiswa aktif |
| **Pascakondisi Gagal** | Data gagal disimpan (misal: NIM kembar), sistem memberikan peringatan |
| **Generalization** | SIA-UC10: Kelola Data Mahasiswa |
| **Collaboration** | - |


| Elemen | Deskripsi |
| :--- | :--- |
| **ID dan Nama** | SIA-UC12: Ubah Data Mahasiswa |
| **Sumber Kebutuhan** | SIA-R11 |
| **Tujuan** | Mengubah atau memperbarui informasi profil/akademik mahasiswa yang sudah ada |
| **Aktor Utama** | Admin Akademik |
| **Pemicu** | Admin memilih opsi "Edit/Ubah" pada salah satu baris data mahasiswa |
| **Prasyarat** | Admin telah berada di halaman SIA-UC10; Data mahasiswa yang ingin diubah ditemukan |
| **Pascakondisi Berhasil** | Perubahan data mahasiswa berhasil diperbarui di dalam database |
| **Pascakondisi Gagal** | Perubahan dibatalkan atau gagal disimpan, data kembali ke status lama |
| **Generalization** | SIA-UC10: Kelola Data Mahasiswa |
| **Collaboration** | - |


| Elemen | Deskripsi |
| :--- | :--- |
| **ID dan Nama** | SIA-UC13: Hapus Data Mahasiswa |
| **Sumber Kebutuhan** | SIA-R11 |
| **Tujuan** | Menghapus data rekaman mahasiswa yang sudah tidak aktif atau salah input dari database |
| **Aktor Utama** | Admin Akademik |
| **Pemicu** | Admin memilih opsi "Hapus" pada data mahasiswa tertentu |
| **Prasyarat** | Admin telah berada di halaman SIA-UC10; Mahasiswa terpilih tidak terikat kelas aktif |
| **Pascakondisi Berhasil** | Data mahasiswa terhapus secara permanen atau statusnya diubah menjadi nonaktif |
| **Pascakondisi Gagal** | Penghapusan ditolak oleh sistem karena melanggar relasi data (*foreign key*) |
| **Generalization** | SIA-UC10: Kelola Data Mahasiswa |
| **Collaboration** | - |
