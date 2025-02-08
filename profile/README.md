# Archana Berry OS  
**Proyek sistem operasi hobi berbasis Unix Kustom (Unix-Like) yang ringan, fleksibel, terintegrasi, dan modularitas tinggi.** 

<img src="https://raw.githubusercontent.com/Archana-Berry-OS/.github/main/profile/orglogo.png" alt="Logo Archana Berry Organization" width="200" />
<img src="https://raw.githubusercontent.com/Archana-Berry-OS/.github/main/profile/oslogo.png" alt="Logo Archana Berry OS" width="1000" />

---
## Proyek masih tahap pengembangan.

---

## Maskot Archana Berry (BLUEBERRY CHAN)
<img src="https://raw.githubusercontent.com/Archana-Berry-OS/.github/main/profile/archanaberry.png" alt="Archana Berry" width="500" />

## Deskripsi  
**Archana Berry OS** adalah sistem operasi hobi (dibuat belajar) modern yang dirancang untuk memberikan efisiensi tinggi dan performa tinggi dengan fitur-fitur unggulan yang cocok untuk berbagai kebutuhan seperti profesional, kantor, konten kreator, gaming, server hosting, hingga penggunaan sehari-hari.  

Sistem operasi ini dibangun dengan filosofi **ringkas, fleksibel, modular**, serta menghadirkan pendekatan baru dalam manajemen sistem dan aplikasi, jauh berbeda dibandingkan OS tradisional seperti Windows, Linux, atau macOS.  

---

## Fitur Utama  
- **Manajemen File dan Aplikasi yang Modular**  
  Archana Berry OS menggunakan format **ABP** (Archana Berry Package) dan **ABPI** (Installer), memudahkan pengguna dalam mengelola aplikasi dengan GUI maupun terminal dan **XABP** (Cross Archana Berry Program) fleksibel pengembangan pakai bahasa pemprograman non native.

- **Fokus pada Efisiensi dan Performa Tinggi**  
  Dengan memanfaatkan *memory management* yang optimal, OS ini sangat cocok untuk. daily driver, gaming dan profesional.  

- **Bahasa Pemrograman Modern**  
  Dibangun menggunakan **Rust** + **C** + **Assembly inline C** kombinasi untuk keamanan dan kecepatan serta efisiensi tinggi, serta mendukung aplikasi berbagai bahasa pemrograman (C, C++, Rust, bahkan Java/Kotlin, Swift, dll).  
 
### **Struktur Direktori OS Archana Berry**

| **Jalur Direktori**      | **Deskripsi**                                                                                                                                                     |
|--------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **/sbin**               | Program biner untuk aplikasi sistem (CoreUtils utama) dari /sbin/archanaberry kemudian disymlink atau dipecah menjadi seperti `mv`, `ls`, `cp`, `touch` dan lainnya.                                                                   |
| **/boot**               | Struktur bootable OS Archana Berry, berisi loader dan kernel.                                                                                                  |
| **/etc**                | Direktori untuk konfigurasi sistem untuk pengaturan sistem, subsistem, tweak, dan konfigurasi lainnya.                                     |
| **/etc/useraccount**    | Direktori untuk konfigurasi setelan desktop, akun pengguna, serta tempat menyimpan sandi.                                     |
| **/archanaberry/**      | Direktori untuk layanan inti dan pengguna root sistem.                                                                                                         |
| **/home/(user)**        | Direktori khusus untuk pengguna dengan isolasi aman antar pengguna, berisi data aplikasi dan konfigurasi personal.                                              |
| **/system/develop**     | Mendukung pengembang dengan library header untuk C/C++/Rust, termasuk sumber kode di dalam folder `include` dan `src`.                                          |
| **/system/base**        | Direktori rollback dan cadangan berupa file `.abb` (Archana Berry Backup File), seperti file mentah OS dan recovery tools.                                      |
| **/system/driver**      | Kumpulan driver khusus untuk OS Archana Berry dengan format `.abd` seperti driver `keyboard.abd` dan `touchscreen.abd`.                                          |
| **/lib**                | Kumpulan library dengan format khusus Archana Berry, seperti `.abdll`, dan `.absll`.                                                                   |
| **/system/kernel**      | Partisi kernel termount dan berisi kernel modul (.abkm), dan kernel library (.abkl) dari partisi kedua.                                                                 || **/system/app**         | Aplikasi sistem bawaan dengan format `.abp`, seperti `calculator.abp`, `filemanager.abp`, dan lainnya.                                                          |
| **/system/config**      | Konfigurasi sistem baik service, init, register, setelan, kernel, os, startup, mounting, loader, dll.                                                         |
| **/system/preference**  | Direktori untuk personalisasi, berisi pengaturan tema, ikon, font, wallpaper, dan tampilan lainnya.                                                            |
| **/cache**              | Direktori untuk file sementara (temp) dan log sistem seperti `dmesg`.                                                                                          |
| **/mnt**                | Direktori untuk mounting storage seperti `usb0`, `cdrom`, dan lainnya.                                                                                         |
| **/storage**            | Storage internal dan eksternal, termasuk `nvme0`, `sdcard0`, dan lainnya.                                                                                      |
| **/proc**               | Sistem file virtual untuk informasi kernel dan proses yang sedang berjalan.                                                                                     |
| **/dev**                | Berisi file device untuk mengakses perangkat keras (block device, karakter device, dll).                                                                       |
| **/var/temp**           | File sementara tambahan untuk kebutuhan sistem.                                                                                                                |
| **/archanaberry/.userdata** | Direktori khusus untuk data pengguna root, berisi aplikasi yang sudah terinstal (`app`) dan data masing-masing aplikasi (`data`).                           |
| **/home/(user)/.userdata** | Direktori khusus untuk data pengguna, berisi aplikasi yang sudah terinstal (`app`) dan data masing-masing aplikasi (`data`).                           |
| **/home/(user)/.bin**   | Direktori khusus untuk aplikasi biner pengguna dengan isolasi aman antar pengguna tertentu dan terpisah dari sistem dan pengguna lain (mirip sbin tetapi versi pengguna biasa).                                        |
| **/etc/os-release**     | File berisi informasi nama OS, rilisan, dan versi Archana Berry.                                                                                               |
| **/system/preference/locale**     | File berisi bahasa sistem baik untuk CLI dan GUI nya.                                                                                              |

- **Dukungan Multibahasa**  
  Dengan file bahasa berbasis teks (`lang.id`, `lang.en`), memungkinkan personalisasi hingga ke level booting dan recovery hingga GUI.  

- **Custom Library Formats**  
  - `.abdll`, `.absll`, `.abkm`, `abkl`,

1. **`.abdll`** - Archana Berry Dynamic Link Library  
   - **MimeType:** `application/x.vnd.archanaberry-dylib`  
   - Format library dynamic link yang memungkinkan pembaruan library tanpa perlu restart sistem. Cocok untuk aplikasi yang memerlukan modularitas tinggi.  

2. **`.absll`** - Archana Berry Static Link Library  
   - **MimeType:** `application/x-vnd.archanaberry-staticlib`  
   - Format library static link yang digunakan untuk aplikasi atau tool yang tidak membutuhkan pembaruan library secara dinamis, cocok untuk pengembangan aplikasi lawas, perubahan dinamis, dan aplikasi library tertentu, hanya saja perlu kompilasi ulang aplikasi.

3. **`.abkm`** - Archana Berry Kernel Module
   - **MimeType:** `application/x-vnd.archanaberry-kmod`
   - Format library untuk ekstensi fitur kernel pada level rendah

4. **`.abkl`** - Archana Berry Kernel Library  
   - **MimeType:** `application/x-vnd.archanaberry-klib`  
   - Format library untuk library khusus dalam sistem kernel

  * Menghadirkan modularitas library unik dengan performa jauh lebih optimal.
 
- **Archana Berry App Formats**
	- `.abp` Archana Berry Program Package **[application/vnd.archanaberry.program.package]**
	- `.abpi` Archana Berry Package Installer **[application/vnd.archanaberry.package.installer]**
	- `.xabp` Cross Archana Berry Program Package **[xapplication/vnd.archanaberry.crosspackage]**

- **Dukungan Gaming**  
  Archana Berry OS dirancang agar porting game, editing, dan aplikasi berbasis grafis menjadi lebih mudah dan ringan.  

---

## Kelebihan  
- **Minimalis dan Cepat**: Tanpa layanan rumit seperti banyak distribusi Linux.
- **Modular**: Bisa menambahkan/mengurangi modul secara internal maupun eksternal dengan mudah.
- **Fleksibel**: Bisa diporting ke Raspberry Pi, Orange Pi, hingga STB TV dan Android Phone.  
- **Integrasi Modern**: Dukungan VTuber tools seperti Live2D/3D dan perlatan konmten kreator.
- **Cocok untuk Pengembangan**: Direct support untuk pengembang dengan library bawaan.
- **Recovery**: Mempermudah pemulihan jika OS kesulitan masuk karena masalah kritis.
- **PSOD**: "Purple Screen Of Dead" Untuk mempermudah analisa kesalahan OS dengan GUI Framebuffer dan kode QR dmesg.
- **No Memory Leak** Bebas kebocoran memory karena dasar OS nya menggunakan bahasa pemrograman **RUST**.
- **BerryX11**: Komposit mirip seperti X11 dan ini jauh lebih ringan dan bersih.

---

## Kebutuhan Sistem  
- Prosesor: Minimal ARM atau x86_64 (Mendukung 32bit dan 64bit)
- RAM: Minimal 1 GB (Direkomendasikan 2 GB untuk performa optimal)  
- Penyimpanan: Minimal 10 GB untuk sistem dasar  

---

## Cara Memulai  
1. Clone repository ini:  
   ```bash
   git clone https://github.com/Archana-Berry-OS/archanaberry-os.git
   ```  
2. Ikuti instruksi di dokumen `INSTALL.md`.  

3. Jalankan pakai mesin virtual atau nyata (actual machine).
---

## Kontributor  
- **Archana Berry** (Pendiri dan Pengembang Utama)  

---

## Lisensi  
Proyek ini dilisensikan sebagian [Public License](https://github.com/Archana-Berry-OS/lisensi/blob/main/README.md).  

---

## Dukungan  
Untuk pertanyaan atau dukungan, silakan buat *issue* di GitHub atau hubungi kami di **archanaberry101originally@gmail.com**.  

--- 

Dengan struktur dan fitur yang inovatif, Archana Berry OS adalah langkah baru menuju sistem operasi masa depan. Mari bergabung dan kembangkan bersama kami!
