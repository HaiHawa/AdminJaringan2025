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

## Chapter 6: Instalasi dan Manajemen Perangkat Lunak



#### Instalasi Sistem Operasi
Distribusi Linux dan FreeBSD menyediakan prosedur sederhana untuk instalasi dasar. Pada perangkat fisik, proses booting dapat dilakukan melalui CD, DVD, atau USB. Sementara itu, mesin virtual dapat memanfaatkan file ISO untuk booting. Instalasi OS dari media lokal menjadi lebih mudah dengan bantuan antarmuka grafis yang memandu pengguna sepanjang proses.



#### Instalasi dari Jaringan
Menginstal OS di banyak komputer menggunakan media lokal kurang efisien karena memakan waktu, berisiko terjadi kesalahan, dan harus dilakukan berulang kali. Alternatif yang lebih praktis adalah instalasi melalui server jaringan, yang umum digunakan di pusat data dan lingkungan cloud.
Salah satu metode yang sering digunakan melibatkan DHCP dan TFTP untuk booting tanpa media fisik. Setelah itu, sistem mengambil file instalasi OS dari server jaringan melalui protokol seperti HTTP, FTP, atau NFS. File instalasi ini dapat disimpan di satu server atau dibagi ke beberapa server berbeda.

Proses instalasi juga bisa dilakukan secara otomatis menggunakan PXE (Preboot eXecution Environment), sebuah standar yang dikembangkan oleh Intel untuk memungkinkan booting melalui jaringan tanpa media penyimpanan tambahan.

PXE berfungsi sebagai OS kecil yang tertanam dalam ROM kartu jaringan. Teknologi ini menyediakan akses jaringan melalui API standar yang dapat dimanfaatkan oleh BIOS sistem. Dengan demikian, boot loader dapat melakukan netboot pada komputer yang mendukung PXE tanpa perlu driver tambahan untuk setiap kartu jaringan.



#### Sistem Manajemen Paket Linux
Menggunakan dua format utama:
- RPM, digunakan oleh Red Hat, CentOS, SUSE, dan Amazon Linux.  
- .deb, digunakan oleh Debian dan Ubuntu. 

Keduanya memiliki fungsi serupa dalam mengelola perangkat lunak di sistem operasi.

Manajemen paket bekerja dalam dua lapisan:
1. Lapisan dasar: Menangani proses instalasi, penghapusan, dan pencarian paket menggunakan rpm (untuk sistem berbasis RPM) dan dpkg (untuk sistem berbasis .deb).
2. Lapisan lanjutan: Bertugas mengunduh paket dari internet, mengelola ketergantungan antar paket, serta melakukan pembaruan sistem. yum,  Yellowdog Updater, Modified, bekerja dengan sistem RPM. sementara APT digunakan pada sistem berbasis .deb, tetapi juga bisa menangani paket RPM.


