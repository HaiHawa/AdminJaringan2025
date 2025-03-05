<div align="center">
  <h1 style="text-align: center;font-weight: bold">Laporan<br>Workshop Administrasi Jaringan<br></h1>
  <h4 style="text-align: center;">Dosen Pengampu : Dr. Ferry Astika Saputra, S.T., M.Sc.</h4>
</div>
<br />
<div align="center">
  <img src="https://upload.wikimedia.org/wikipedia/id/4/44/Logo_PENS.png" alt="Logo PENS">
  <h3 style="text-align: center;">Disusun Oleh :</h3>
  <p style="text-align: center;">
    <strong>Hawa Kharisma Zahara (3123500010)</strong>
  </p>
<h3 style="text-align: center;line-height: 1.5">Politeknik Elektronika Negeri Surabaya<br>Departemen Teknik Informatika Dan Komputer<br>Program Studi D3 Teknik Informatika<br>2025/2026</h3>
  <hr>
</div>
<br>

---

# Chapter 6: Instalasi dan Manajemen Perangkat Lunak



### Instalasi Sistem Operasi
Distribusi Linux dan FreeBSD menyediakan prosedur sederhana untuk instalasi dasar. Pada perangkat fisik, proses booting dapat dilakukan melalui CD, DVD, atau USB. Sementara itu, mesin virtual dapat memanfaatkan file ISO untuk booting. Instalasi OS dari media lokal menjadi lebih mudah dengan bantuan antarmuka grafis yang memandu pengguna sepanjang proses.


### Instalasi dari Jaringan  
Menginstal OS di banyak komputer dengan media lokal kurang efisien karena memakan waktu, rawan kesalahan, dan harus diulang berkali-kali. Cara yang lebih praktis adalah instalasi melalui server jaringan, yang sering digunakan di pusat data dan lingkungan cloud.  

Salah satu metode yang umum digunakan adalah booting tanpa media fisik menggunakan DHCP dan TFTP. Setelah itu, sistem mengunduh file instalasi OS dari server jaringan melalui HTTP, FTP, atau NFS. File ini bisa disimpan di satu server atau dibagi ke beberapa server berbeda.  

Instalasi juga bisa dilakukan otomatis menggunakan PXE (Preboot eXecution Environment), sebuah standar dari Intel yang memungkinkan booting melalui jaringan tanpa media penyimpanan tambahan.  

PXE bekerja seperti OS kecil yang tersimpan di ROM kartu jaringan. Teknologi ini menyediakan akses jaringan melalui API standar yang bisa digunakan BIOS. Dengan PXE, komputer yang mendukung fitur ini bisa booting langsung dari jaringan tanpa perlu driver tambahan untuk kartu jaringan.

 <img src="images/1.1.png">

### Sistem Manajemen Paket Linux
Menggunakan dua format utama:
- **RPM**, digunakan oleh Red Hat, CentOS, SUSE, dan Amazon Linux.  
- **.deb**, digunakan oleh Debian dan Ubuntu. 

Keduanya memiliki fungsi serupa dalam mengelola perangkat lunak di sistem operasi.

Manajemen paket bekerja dalam dua lapisan:
1. Lapisan dasar: Menangani proses instalasi, penghapusan, dan pencarian paket menggunakan **rpm** (untuk sistem berbasis RPM) dan **dpkg** (untuk sistem berbasis .deb).
2. Lapisan lanjutan: Bertugas mengunduh paket dari internet, mengelola ketergantungan antar paket, serta melakukan pembaruan sistem. **yum**,  Yellowdog Updater, Modified, bekerja dengan sistem **RPM**. sementara **APT** digunakan pada sistem berbasis **.deb**, tetapi juga bisa menangani paket RPM.

### Manajemen Paket Tingkat Tinggi
Alat manajemen paket tingkat tinggi sering digunakan untuk mengelola paket, seperti instalasi, penghapusan, dan pembaruan. Selain itu, alat ini juga dapat digunakan untuk mencari serta menampilkan daftar paket yang terinstal di sistem.

#### Repositori Paket

Repositori paket Linux dikelola oleh distributor dan terhubung dengan sistem manajemen paket. Konfigurasi default biasanya mengarah ke server web atau FTP milik distributor. Dalam repositori, terdapat : 

- _rilis_ yang berisi kumpulan paket yang konsisten
- _komponen_ yang merupakan bagian dari rilis.
- _arsitektur_ yaitu jenis perangkat keras yang dapat menjalankan paket yang sama. Arsitektur adalah contoh rilis, misalnya, arsitektur i386 dari rilis Fedora 20.

#### APT: Alat Paket Tingkat Lanjut

APT adalah sekumpulan alat untuk mengelola paket Debian dan merupakan sistem manajemen paket yang paling umum digunakan pada sistem berbasis Debian. Berikut beberapa alat yang termasuk dalam APT:

- **apt-get** : Alat baris perintah untuk mengelola paket, seperti instalasi, penghapusan, dan pembaruan.
- **apt-cache** : Alat untuk mencari dan menelusuri cache paket APT.
- **apt-file** : Alat untuk mencari file dalam paket.
- **apt-show-versions** : Alat untuk menampilkan versi paket yang tersedia.
- **aptitude** : Antarmuka tingkat tinggi untuk sistem manajemen paket, menawarkan fungsi yang lebih luas dibandingkan apt-get.
- **apt-mirror** : Alat untuk membuat salinan (mirror) repositori paket.

Pada sistem Ubuntu, disarankan untuk mengabaikan **dselect**, karena alat ini hanya berfungsi sebagai antarmuka untuk sistem manajemen paket Debian.


#### yum: Yellowdog Updater, Modified

**yum** adalah alat manajemen paket berbasis RPM yang menangani instalasi, pembaruan, dan penghapusan paket dengan menyelesaikan ketergantungan secara otomatis. Selain mengelola paket dari repositori, yum juga dapat digunakan melalui baris perintah untuk operasi paket individual.

### Pelokalan dan Konfigurasi Perangkat Lunak
Menyesuaikan sistem dengan lingkungan lokal atau cloud adalah tantangan utama dalam administrasi sistem. Agar tidak menimbulkan masalah di kemudian hari, proses ini harus dilakukan dengan cara yang terstruktur, terdokumentasi, dan bisa diulang. Pendekatan ini mencegah sistem menjadi terlalu unik (snowflake system), yang dapat menyulitkan pemulihan saat terjadi kegagalan. Dengan strategi yang tepat, sistem akan lebih stabil, mudah dikelola, dan cepat dipulihkan jika terjadi masalah.

### Kesimpulan:  

- Instalasi dan manajemen perangkat lunak dalam sistem Linux memerlukan pendekatan yang efisien dan terstruktur. 
- Instalasi OS dapat dilakukan melalui media lokal atau jaringan, dengan metode seperti PXE untuk otomatisasi
- Pengelolaan perangkat lunak menggunakan sistem manajemen paket berbasis **RPM** atau **.deb**, dengan alat seperti **yum** dan **APT** untuk menangani instalasi, pembaruan, serta ketergantungan paket. 
- Repositori paket menjadi sumber utama perangkat lunak, yang dikategorikan berdasarkan _rilis_, _komponen_, dan _arsitektur_. 
- Pelokalan dan konfigurasi sistem harus dilakukan secara sistematis untuk mencegah sistem yang sulit dikelola dan dipulihkan.

