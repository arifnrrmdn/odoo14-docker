# Setup Environment Development Odoo 14 di Docker

Panduan ini menjelaskan langkah-langkah untuk melakukan setup lingkungan pengembangan **Odoo 14** menggunakan **Docker**. Semua pengaturan dilakukan dengan konfigurasi standar untuk pengembangan aplikasi berbasis Docker.

## **Lingkungan Pengembangan**

### **WSL (Windows Subsystem for Linux)**
- **Version**: 2.5.9.0
- **Kernel Version**: 6.6.87.2-1
- **WSLg Version**: 1.0.66
- **MSRDC Version**: 1.2.6074
- **Direct3D Version**: 1.611.1-81528511
- **DXCore Version**: 10.0.26100.1-240331-1435.ge-release
- **Windows Version**: 10.0.26100.3194

### **Docker**
- **Docker Engine Version**: 27.5.1, build 27.5.1-0ubuntu3~24.04.2

### **Docker Compose**
- **Version**: 1.29.2, build unknown

## **Langkah-langkah Setup**

1. **Instalasi Docker Desktop**
    - Unduh dan instal **Docker Desktop** versi 27.5.1 pada Windows, yang mendukung integrasi dengan WSL 2.
    - Docker Compose akan diinstal secara otomatis bersama dengan Docker Desktop.

2. **Konfigurasi Docker Compose untuk Odoo 12**
    - Siapkan file konfigurasi `docker-compose.yml` untuk menjalankan **Odoo 12** dan **PostgreSQL** dalam container terpisah.

3. **Pengaturan Volume dan Jaringan**
    - Pastikan volume dan jaringan dikonfigurasi dengan benar agar data Odoo dan PostgreSQL dapat dipertahankan di container terpisah.

4. **Verifikasi Versi Docker dan Docker Compose**
    - Verifikasi versi Docker dan Docker Compose yang terinstal menggunakan perintah:
      ```bash
      docker --version
      docker-compose --version
      ```

5. **Jalankan Docker Compose**
    - Jalankan perintah berikut untuk memulai container:
      ```bash
      docker-compose up
      ```
    - Setelah container berjalan, Odoo dapat diakses melalui `http://localhost:2512`.

6. **Debugging dan Monitoring**
    - Jika terjadi masalah, lakukan debugging dengan melihat log container menggunakan:
      ```bash
      docker logs <nama-container>
      ```
    - Pastikan kedua container (Odoo dan PostgreSQL) berjalan tanpa masalah.

## **Hasil Setup**
- **Odoo 12** dapat dijalankan pada port yang telah dikonfigurasi.
- **PostgreSQL** berjalan di container terpisah dan terhubung dengan Odoo.

## **Screenshot**
![](https://github.com/arifnrrmdn/odoo14-docker/blob/main/images/1.png)
![](https://github.com/arifnrrmdn/odoo14-docker/blob/main/images/2.png)
![](https://github.com/arifnrrmdn/odoo14-docker/blob/main/images/3.png)
  
## **Kesimpulan**
Dengan menggunakan Docker versi **27.5.1** dan Docker Compose versi **1.29.2**, pengaturan **Odoo 12** dapat dilakukan dengan lancar di lingkungan pengembangan berbasis WSL 2. Konfigurasi ini menyediakan cara yang efisien dan mudah untuk menjalankan Odoo dalam container terisolasi.

## **Referensi**
- [Dokumentasi Odoo](https://www.odoo.com/)
- [Docker](https://www.docker.com/)
- [Docker Compose](https://docs.docker.com/compose/)


---
