# Archana Berry OS  
**Proyek sistem operasi hobi berbasis Unix Kustom (Unix-Like) yang ringan, fleksibel, terintegrasi, dan modularitas tinggi.** 

![Logo Archana Berry OS](https://github.com/Archana-Berry-OS/assets/logo.png)  

---
## Proyek masih tahap pengembangan.

---

## Deskripsi  
**Archana Berry OS** adalah sistem operasi modern yang dirancang untuk memberikan efisiensi tinggi dan performa tinggi dengan fitur-fitur unggulan yang cocok untuk berbagai kebutuhan seperti profesional, kantor, konten kreator, gaming, server hosting, hingga penggunaan sehari-hari.  

Sistem operasi ini dibangun dengan filosofi **ringkas, fleksibel, modular**, serta menghadirkan pendekatan baru dalam manajemen sistem dan aplikasi, jauh berbeda dibandingkan OS tradisional seperti Windows, Linux, atau macOS.  

---

## Fitur Utama  
- **Manajemen File dan Aplikasi yang Modular**  
  Archana Berry OS menggunakan format **ABP** (Archana Berry Package) dan **ABPI** (Installer), memudahkan pengguna dalam mengelola aplikasi dengan GUI maupun terminal dan **XABP** (Cross Archana Berry Program) fleksibel pengembangan pakai bahasa pemprograman non native.

- **Fokus pada Efisiensi dan Performa Tinggi**  
  Dengan memanfaatkan *memory management* yang optimal, OS ini sangat cocok untuk. daily driver, gaming dan profesional.  

- **Bahasa Pemrograman Modern**  
  Dibangun menggunakan **Rust** untuk keamanan dan kecepatan, serta mendukung berbagai bahasa pemrograman (C, C++, Rust, bahkan Java/Kotlin, Swift, dll).  

- **Sistem Berkas yang Terorganisir**  
  - `/archanaberry/` untuk layanan inti dan pengguna root sistem.  
  - `/home/(user)/` untuk pengguna, memastikan isolasi yang aman antar user.  
  - `/system/develop/` mendukung pengembang dengan library header C/C++/Rust bawaan.
  - `/system/base` untuk rollback dan cadangan sumber kode os dalam bentuk .abb (Archana Berry Backup file).
  - `/system/driver` untuk kumpulan driver khusus Archana Berry (.abd).
  - `/lib` untuk kumpulan library dengan format kustom untuk Archana Berry.
  - `/system/app` untuk kumpulan aplikasi sistem bawaan GUI (.abp)

- **Dukungan Multibahasa**  
  Dengan file bahasa berbasis teks (`lang.id`, `lang.en`), memungkinkan personalisasi hingga ke level booting dan recovery hingga GUI.  

- **Custom Library Formats**  
  - `.abdll`, `.absll`, `.abl`, `.abo`, `aboll`, dll, menghadirkan modularitas unik dengan performa optimal.  

- **Dukungan Gaming**  
  Archana Berry OS dirancang agar porting game, editing, dan aplikasi berbasis grafis menjadi lebih mudah.  

---

## Kelebihan  
- **Minimalis dan Cepat**: Tanpa layanan rumit seperti banyak distribusi Linux.  
- **Fleksibel**: Bisa diporting ke Raspberry Pi, Orange Pi, hingga STB TV.  
- **Integrasi Modern**: Dukungan VTuber tools seperti Live2D/3D dan perlatan konmten kreator.
- **Cocok untuk Pengembangan**: Direct support untuk pengembang dengan library bawaan.  

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
Proyek ini dilisensikan di bawah [MIT License](LICENSE).  

---

## Dukungan  
Untuk pertanyaan atau dukungan, silakan buat *issue* di GitHub atau hubungi kami di **archanaberry101originally@gmail.com**.  

--- 

Dengan struktur dan fitur yang inovatif, Archana Berry OS adalah langkah baru menuju sistem operasi masa depan. Mari bergabung dan kembangkan bersama kami!
