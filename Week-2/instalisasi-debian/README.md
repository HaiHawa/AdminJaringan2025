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

Instalisasi Debian dan Oracle Virtual Box di Linux

Solve LAN Wired Not Connected

<img src="images/1.jpg">

Perintah sudo dhclient -v digunakan untuk meminta atau memperbarui alamat IP dari server DHCP (Dynamic Host Configuration Protocol).







Clone Github

Install git

<img src="images/2.jpg">

sudo apt install git
Perintah sudo apt install git digunakan untuk menginstal Git pada sistem berbasis Debian/Ubuntu menggunakan APT (Advanced Package Tool).

Setelah instalasi, bisa cek apakah Git sudah terpasang dengan:
git --version



<img src="images/3.jpg">


Selanjutnya melakukan git clone dengan perintah dibawah ini

git clone https://github.com/ferryastika/unix-and-linux-sysadmin-notes.git



Cek OS

<img src="images/4.png">
Perintah lsb_release -a digunakan untuk menampilkan informasi lengkap tentang sistem operasi Linux yang sedang digunakan.




Download VirtualBox 

<img src="images/5.jpg">
https://www.virtualbox.org/wiki/Linux_Downloads
Download Virtual sesuai dengan OS yang digunakan. Saat ini komputer yang saya pakai menggunakan OS 12 jadi unduh Debian 12.

Download ISO Debian 12
<img src="images/6.jpg">


https://www.debian.org/download
ISO di VirtualBox adalah file image disk yang digunakan untuk menginstal atau menjalankan sistem operasi tanpa CD/DVD fisik. File ini berguna untuk instalasi OS, booting Live OS, serta recovery & maintenance. 

Install VirtualBox

<img src="images/7.jpg">


sudo dpkg -i virtualbox-7.1_7.1.6-167084~Debian~bookworm_amd64.deb

Perintah diatas digunakan untuk menginstal paket VirtualBox secara manual menggunakan dpkg di sistem berbasis Debian.

<img src="images/8.jpg">

sudo apt install libxcb-cursor0
Perintah diatas digunakan untuk menginstal pustaka libxcb-cursor0 di sistem berbasis Debian/Ubuntu


Solving Error VirtualBox
<img src="images/9.png">

Solve error diatas menggunakakn perintah:

<img src="images/10.jpg">

Perintah diatas digunakan untuk menambahkan pengguna ke grup vboxusers agar dapat menggunakan fitur USB di VirtualBox.


Oracle VirtualBox Manager



Membuat New Virtual Machine, berikut:


<img src="images/11.jpg">





Pertama mengatur nama, lokasi penyimpanan, serta memilih file ISO untuk instalasi. 
<img src="images/12.png">

Kedua, mengatur username, password, hostname, dan domain. 


<img src="images/13.png">







Ketiga, mengatur spesifikasi RAM dan CPU seperti dibawah ini.

<img src="images/14.png">
 Selanjutnya, menentukan konfigurasi hard disk virtual

<img src="images/15.png">



Terakhir, dapat meninjau kembali konfigurasi yang telah dipilih sebelum menekan tombol "Finish" untuk memulai proses pembuatan. Jika sudah sesuai, maka klik Finish.

<img src="images/16.png">














Kernel Error

<img src="images/17.png">

Gunakan perintah berikut untuk memperbaiki error pada kernel:
sudo apt update
sudo apt install dkms build-essential linux-headers-$(uname -r)
sudo /sbin/vboxconfig

<img src="images/18.png">
<img src="images/19.png">








Run Virtual Machine


Jalankan proses instalasi dan tunggu hingga Debian di VM terpasang serta terinisialisasi dengan sempurna.

<img src="images/20.jpg">
<img src="images/21.jpg">








Jika tampilan sudah sesuai dengan gambar di bawah, berarti instalasi Debian 12 di VirtualBox telah berhasil.

<img src="images/22.png">

Lanjutkan dengan mengklik "Next" hingga selesai. Jika tampilan sudah seperti gambar di bawah, berarti Debian di VirtualBox siap digunakan.

<img src="images/23.png">



