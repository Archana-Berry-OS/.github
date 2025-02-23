# Archana Berry OS  
**Proyek sistem operasi hobi berbasis Unix Kustom (Unix-Like) yang ringan, fleksibel, terintegrasi, dan memiliki modularitas tinggi.**

<img src="https://raw.githubusercontent.com/Archana-Berry-OS/.github/main/profile/orglogo.png" alt="Logo Archana Berry Organization" width="200" />
<img src="https://raw.githubusercontent.com/Archana-Berry-OS/.github/main/profile/oslogo.png" alt="Logo Archana Berry OS" width="1000" />

---

## Proyek masih tahap pengembangan.

---

## Maskot Archana Berry (BLUEBERRY CHAN)
<img src="https://raw.githubusercontent.com/Archana-Berry-OS/.github/main/profile/archanaberry.png" alt="Archana Berry" width="500" />

---

## Deskripsi  
**Archana Berry OS** adalah sistem operasi hobi (diciptakan untuk belajar dan eksplorasi) modern yang dirancang untuk memberikan efisiensi serta performa tinggi. OS ini cocok untuk berbagai kebutuhan, mulai dari profesional dan kantor, konten kreator, gaming, server hosting, hingga penggunaan sehari-hari.  
Sistem operasi ini dibangun dengan filosofi **ringkas, fleksibel, dan modular**, serta menghadirkan pendekatan baru dalam manajemen sistem dan aplikasi—yang berbeda dari OS tradisional seperti Windows, Linux, maupun macOS.

---

## Fitur Utama  
- **Manajemen File dan Aplikasi yang Modular:**  
  OS ini menggunakan format aplikasi khusus seperti:  
  - **ABP (Archana Berry Program)**  
  - **ABPI (Package Installer)**  
  - **XABP (Cross Archana Berry Program)**  
  untuk memudahkan pengelolaan aplikasi baik melalui antarmuka GUI maupun melalui terminal.

- **Fokus pada Efisiensi dan Performa Tinggi:**  
  Dengan manajemen memori yang optimal dan eksekusi biner native melalui format **BEFB (Berry Executable File Binary)**, OS ini sangat cocok sebagai daily driver, untuk gaming, dan aplikasi profesional.

- **Bahasa Pemrograman Modern:**  
  Dibangun menggunakan kombinasi **Rust, C, dan Assembly**, sehingga menjamin keamanan tinggi (tanpa memory leak) serta kecepatan eksekusi yang optimal. OS ini juga mendukung pengembangan aplikasi dalam berbagai bahasa seperti C, C++, Rust, Java, Kotlin, Python, JavaScript, dan TypeScript melalui runtime khusus.

- **Struktur dan Format Library Kustom:**  
  - **.abdll:** Archana Berry Dynamic Link Library, untuk linking dinamis di user space.  
  - **.absll:** Archana Berry Static Link Library, untuk linking statis yang meningkatkan performa dan mengurangi overhead runtime.  
  - **.abkm:** Archana Berry Kernel Module, modul kernel dinamis (setara dengan .mod di Linux).  
  - **.abkl:** Archana Berry Kernel Library, library kernel untuk fungsi inti (setara dengan .ko di Linux).

- **Eksekusi Berlapis:**  
  OS ini membagi ruang eksekusinya menjadi tiga lapisan:
  1. **Kernel Space:** Tempat eksekusi inti OS, driver, dan modul-modul kernel.  
  2. **Runtime Native Space (RNS):** Lapisan penghubung yang dikelola oleh **ABRT (Archana Berry Runtime)**, yang secara cerdas menangani eksekusi aplikasi—baik native (BEFB) maupun aplikasi runtime (ABP, XABP, ABPI)—dengan dukungan JIT dan AOT.  
  3. **User Space:** Tempat aplikasi biasa dijalankan, terpisah secara ketat agar tidak mengganggu sistem inti.

- **Keamanan Terintegrasi:**  
  Dengan menggunakan **SEUNRA (Security Enchanted Unique for Native and Runtime + AppArmor)**, OS ini memiliki mekanisme keamanan canggih yang mengamankan library sensitif di user space dan kernel space, serta menyediakan isolasi melalui **BerrySandbox**.

- **Dukungan Multiplatform dan Subsistem:**  
  Melalui subsistem seperti:  
  - **ABSAG:** Archana Berry Subsystem for Android with Google Framework (kompatibilitas hampir 100% untuk aplikasi Android)  
  - **ABSLA:** Archana Berry Subsystem for Linux Additional (untuk plugin GNU/Linux)  
  - **ABSUC:** Archana Berry Subsystem for Unix Coreutils  
  - **ABSW:** Archana Berry Subsystem for Windows  
  - **ABSA:** Archana Berry Subsystem for Apple  
  - **ABSDE:** Archana Berry Subsystem for DOS Environment  
  OS ini mampu menjalankan aplikasi dari berbagai ekosistem tanpa bergantung pada virtualisasi berat.

- **Antarmuka Pengguna yang Elegan:**  
  Dengan **BerryX11** sebagai sistem komposit grafis (mirip X11) yang ringan, OS ini menawarkan antarmuka yang bersih dan mudah dikustomisasi.

- **Fitur Recovery dan Diagnostik:**  
  Dilengkapi dengan **PSOD (Purple Screen of Death)** yang menampilkan kode QR, emoji, dan pesan diagnostik untuk memudahkan perbaikan dan analisis kesalahan.

- **Ekosistem Pengembangan dan Instalasi:**  
  - **ABPM (Archana Berry Package Manager):** Mengelola paket aplikasi dan modul dependensi, mendukung instalasi offline melalui ABPI, serta ekstensi modul seperti `nodemodule`, `pymodules`, dan `gradlewm` yang disimpan di `/home/(user)/.extmodules/`.

---

## Struktur Direktori OS Archana Berry

| **Jalur Direktori**                | **Deskripsi**                                                                                                                                                     |
|------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **/archanaberry/**                | Direktori untuk layanan inti dan pengguna root sistem.                                                                                                         |
| **/archanaberry/.userdata**       | Direktori khusus untuk data pengguna root, berisi aplikasi yang sudah terinstal (`app`) dan data masing-masing aplikasi (`data`).                           |
| **/boot**                         | Struktur bootable OS Archana Berry, berisi loader dan kernel.                                                                                                  |
| **/cache**                        | Direktori untuk file sementara (temp) dan log sistem seperti `dmesg`.                                                                                          |
| **/dev**                          | Berisi file device untuk mengakses perangkat keras (block device, karakter device, dll).                                                                       |
| **/etc**                          | Direktori untuk konfigurasi sistem untuk pengaturan sistem, subsistem, tweak, dan konfigurasi lainnya.                                                         |
| **/etc/useraccount**              | Direktori untuk konfigurasi setelan desktop, akun pengguna, serta tempat menyimpan sandi.                                                                     |
| **/home/(user)**                  | Direktori khusus untuk pengguna dengan isolasi aman antar pengguna, berisi data aplikasi dan konfigurasi personal.                                              |
| **/home/(user)/.bin**             | Direktori khusus untuk aplikasi biner pengguna dengan isolasi aman antar pengguna tertentu dan terpisah dari sistem dan pengguna lain (mirip sbin tetapi versi pengguna biasa). |
| **/home/(user)/.userdata**        | Direktori khusus untuk data pengguna, berisi aplikasi yang sudah terinstal (`app`) dan data masing-masing aplikasi (`data`).                                 |
| **/mnt**                          | Direktori untuk mounting storage seperti `usb0`, `cdrom`, dan lainnya.                                                                                         |
| **/proc**                         | Sistem file virtual untuk informasi kernel dan proses yang sedang berjalan.                                                                                     |
| **/sbin**                         | Program biner untuk aplikasi sistem (CoreUtils utama) dari `/sbin/archanaberry`, kemudian disymlink atau dipecah menjadi perintah seperti `mv`, `ls`, `cp`, `touch`, dll. |
| **/storage**                      | Storage internal dan eksternal, termasuk `nvme0`, `sdcard0`, dan lainnya.                                                                                      |
| **/system/app**                   | Aplikasi sistem bawaan dengan format `.abp`, seperti `calculator.abp`, `filemanager.abp`, dan lainnya.                                                          |
| **/system/base**                  | Direktori rollback dan cadangan berupa file `.abb` (Archana Berry Backup File), seperti file mentah OS dan recovery tools.                                      |
| **/system/config**                | Konfigurasi sistem, termasuk pengaturan service, init, register, setelan, kernel, OS, startup, mounting, loader, dll.                                             |
| **/system/config/os-release**     | File berisi informasi nama OS, rilisan, dan versi Archana Berry.                                                                                               |
| **/system/develop**               | Mendukung pengembang dengan library header untuk C/C++/Rust, termasuk sumber kode di dalam folder `include` dan `src`.                                          |
| **/system/driver**                | Kumpulan driver khusus untuk OS Archana Berry dengan format `.abd` seperti `keyboard.abd` dan `touchscreen.abd`.                                               |
| **/system/kernel**                | Partisi kernel yang berisi kernel modul (`.abkm`) dan kernel library (`.abkl`), yang di-load dari partisi kedua.                                                 |
| **/system/lib**                   | Kumpulan library dengan format khusus Archana Berry, seperti **.abdll** (dinamis) dan **.absll** (statis).                                                       |
| **/system/preference**            | Direktori untuk personalisasi, berisi pengaturan tema, ikon, font, wallpaper, dan tampilan lainnya.                                                            |
| **/system/preference/locale**     | File berisi bahasa sistem untuk CLI dan GUI.                                                                                                                   |
| **/var/temp**                     | File sementara tambahan untuk kebutuhan sistem.                                                                                                                |

---

## Format Library & Eksekusi Aplikasi

- **Format Library:**  
  - **.abdll:** Archana Berry Dynamic Link Library (digunakan untuk linking dinamis di user space).  
  - **.absll:** Archana Berry Static Link Library (digunakan untuk linking statis di aplikasi atau BEFB).  
  - **.abkm:** Archana Berry Kernel Module (setara dengan .mod, digunakan untuk ekstensi kernel yang dapat dimuat secara dinamis).  
  - **.abkl:** Archana Berry Kernel Library (setara dengan .ko di Linux, untuk library inti kernel).

- **Format Aplikasi:**  
  - **BEFB (Berry Executable File Binary):** Format biner native yang dijalankan tanpa runtime tambahan, mirip dengan ELF di Linux.  
  - **ABP, XABP, ABPI:** Aplikasi yang dijalankan melalui **ABRT (Archana Berry Runtime)** dengan dukungan AOT dan JIT, serta integrasi API sistem.

- **Loader:**  
  - **User Space Loader:** `/system/lib/libarchanaberry32.abdll` untuk BEFB32 (32-bit) dan `/system/lib/libarchanaberry64.abdll` untuk BEFB64 (64-bit) berfungsi untuk memuat aplikasi di user space.  
  - **Kernel Space Loader:** `/system/lib/libsysarchanaberry32.abdll` dan `/system/lib/libsysarchanaberry64.abdll` digunakan untuk memuat library dan modul yang berjalan di kernel space.

- **Penamaan Dinamis Library:**  
  Loader secara otomatis dapat mencari dan memuat library tambahan dengan prefix:
  - **User Space:** `"libab<nama>"`, `"libberry<nama>"`, atau `"libarchanaberry.<nama>"`.
  - **Kernel Space:** `"libabk<nama>"`, `"libberryk<nama>"`, `"libsys.<nama>"`, atau `"lib<nama>"`.
  
  Pendekatan ini memastikan fitur dan modul dapat ditambahkan secara dinamis, serupa dengan mekanisme LKM di Linux, sambil tetap menjaga keamanan dan integritas sistem.

---

## Eksekusi Aplikasi & Runtime

- **Native Execution (BEFB):**  
  Aplikasi yang dikompilasi sebagai BEFB dijalankan secara native melalui **ABBL (Archana Berry Binary Loader)**, tanpa memerlukan runtime tambahan, cocok untuk layanan sistem, program inti, dan aplikasi CLI.

- **Runtime Execution (ABRT):**  
  Aplikasi yang berupa ABP, XABP, dan ABPI dijalankan melalui **ABRT (Archana Berry Runtime)**, yang mendukung AOT dan JIT untuk fleksibilitas tinggi serta integrasi mendalam dengan API dan subsistem OS.

---

## Subsistem Eksternal dan Modul Tambahan

- **Subsistem:**  
  OS mendukung berbagai subsistem untuk kompatibilitas lintas platform, antara lain:
  - **ABSW:** Archana Berry Subsystem for Windows.
  - **ABSA:** Archana Berry Subsystem for Apple.
  - **ABSAG:** Archana Berry Subsystem for Android (dengan dukungan Google Framework, hampir 100% kompatibel).
  - **ABSLA:** Archana Berry Subsystem for Linux Additional.
  - **ABSUC:** Archana Berry Subsystem for Unix Coreutils.
  - **ABSDE:** Archana Berry Subsystem for DOS Environment (dengan basis FreeDOS).

- **Ekstensi Modul di ABPM:**  
  Modul eksternal seperti `nodemodule`, `pymodules`, atau `gradlewm` dapat diinstal melalui perintah ABPM untuk memenuhi kebutuhan runtime khusus, dan disimpan di `/home/(user)/.extmodules/`.

---

## Kebutuhan Sistem  
- **Prosesor:** Minimal ARM atau x86_64 (mendukung 32-bit dan 64-bit).  
- **RAM:** Minimal 1 GB (Direkomendasikan 2 GB untuk performa optimal).  
- **Penyimpanan:** Minimal 10 GB untuk sistem dasar.

---

## Cara Memulai  
1. Clone repository ini:  
   ```bash
   git clone https://github.com/Archana-Berry-OS/archanaberry-os.git
   ```  
2. Ikuti instruksi di dokumen `INSTALL.md`.  
3. Jalankan pada mesin virtual atau perangkat nyata (actual hardware).

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

**Slogan:**  
"Sistem Operasi yang Fleksibel dan Andal."
"A Flexible and Reliable Operating System."

---

## Note 

- **Aplikasi Native (BEFB):**  
  - Format biner BEFB dijalankan secara native melalui ABBL, tanpa runtime ABRT, cocok untuk layanan inti dan aplikasi CLI (aplikasi yang ditulis dalam Rust, C, C++).  

- **Aplikasi Runtime (ABP, XABP, ABPI):**  
  - Dijalankan melalui ABRT (Runtime Native Space) yang mendukung AOT/JIT, sehingga memberikan fleksibilitas dan kinerja tinggi.  
  - ABP untuk aplikasi native yang terkompilasi (aplikasi yang ditulis dalam Rust, C, C++).  
  - XABP untuk aplikasi berbasis skrip (seperti aplikasi menggunakan ABS, JavaScript, atau TypeScript) yang dapat berjalan melalui interpreter atau dengan kompilasi runtime.  
  - ABPI sebagai paket instalasi yang mempermudah penambahan modul, driver, atau framework ke sistem.

- **Format Library dan Modul:**  
  - **.abdll:** Library dinamis untuk user space.  
  - **.absll:** Library statis untuk aplikasi yang di-link langsung ke binary.  
  - **.abkm:** Modul kernel yang dapat dimuat dinamis (setara .mod).  
  - **.abkl:** Library kernel (setara .ko) untuk fungsi inti kernel.

- **Loader dan Penamaan Dinamis:**  
  - Loader di user space terdapat di `/system/lib/libarchanaberry32.abdll` dan `/system/lib/libarchanaberry64.abdll`, sedangkan loader untuk kernel space ada di `/system/lib/libsysarchanaberry32.abdll` dan `/system/lib/libsysarchanaberry64.abdll`.  
  - Penamaan untu library dinamis menggunakan prefix seperti "libab", "libberry", "libarchanaberry" untuk bagian userspace 
  - Penamaan untuk library kernelspace menggunakan nama prefiks seperti "libabk", "libberryk", "libsys".
