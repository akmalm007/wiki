---
title: Mengapa CachyOS?
description: Mengapa CachyOS mungkin lebih baik untuk Anda
tableOfContents:
  minHeadingLevel: 1
  maxHeadingLevel: 4
---

CachyOS adalah distribusi Arch Linux yang berfokus pada performa didesain untuk memberikan kestabilan, efisiensi, dan lingkungan komputasi yang ramah pengguna. Lalu menawarkan kekuatan penuh dan fleksibilitas dengan sistem *rolling-release*, diperkuat dengan optimasi tinggi dan seperangkat alat bantu yang mempermudah pengalaman pengguna baik untuk pengguna awam dan berpengalaman.

## Performa dan Optimasi

### Paket dan Repositori yang Dioptimalkan

CachyOS menawarkan banyak pilihan [paket yang dioptimalkan](https://packages.cachyos.org/) secara khusus untuk berbagai arsitektur CPU yang terbaru, termasuk sistem `x86-64-v3`, `x86-64-v4`, dan `Zen4+`, memastikan perangkat lunak yang dibuat memakai seluruh kemampuan dari kapabilitas perangkat keras untuk performa yang signifikan.

Untuk informasi lebih lanjut mengenai optimasi repositori milik kami, lihat panduan lengkap kami [**Repositori yang Dioptimalkan.**](/id/features/optimized_repos)

### Kernel Kustom yang Disetel untuk Performa dan Stabilitas

Selain kumpulan *patch* dasar kernel CachyOS yang menyetel berbagai parameter kernel untuk meningkatkan responsivitas desktop, CachyOS memilih kumpulan *patch* yang belum masuk ke *mainline* atau tidak disertakan dalam revisi stabil kernel.

Oleh karena itu, *patch* ini menjalani pengujian internal sebelum dirilis kepada pengguna untuk memastikan stabilitas tidak terpengaruh. Untuk daftar lengkap *patch* yang disediakan CachyOS, lihat [Kernel](/id/features/kernel).

### Dukungan Penjadwal CPU Kustom

CachyOS memasukan kernel dengan optimasi penjadwalan CPU terbaru untuk memastikan kelancaran da dan dekstop yang interaktif, bahkan dengan beban yang berat.

* **EEVDF (penjadwalan bawaan dari Linux kernel):** Meskipun bagus untuk *throughput* pada umumnya, CachyOS kernel memasukan kustom **[EEVDF yang bisa diatur](https://github.com/CachyOS/linux/blob/6.15/cachy/kernel/sched/fair.c#L79-81)** untuk meningkatkan reponsinitas dekstop.

* **[BORE](https://github.com/firelzrd/bore-scheduler) (Burst-Oriented Response Enhancer):** Bagi pengguna yang membutuhkan interaktivitas maksimal, kernel kami mendukung penjadwalan BORE, sebuah *patch* yang meningkatkan EEVDF dalam memberikan pengalaman yang lebih lancar ketika bebankerja yang intensif.

Informasi lebih lanjut tentang kernels yang ditawarkan oleh CachyOS and *sched-ext framework*, lihat **[Kernel](/features/kernel)** dan **[sched-ext](/configuration/sched-ext)** dokumentasi.

## Alat yang ramah pengguna dan kustomisasi

### [Deteksi Perangkat Keras](/features/chwd)

CachyOS menyertakan alat deteksi perangkat keras yang secara otomatis mengidentifikasi dan memasang *driver* serta paket yang diperlukan untuk setiap sistem. Dengan ini tidak perlu mencari *driver* secara manual, sehingga menghemat waktu dan tenaga setelah instalasi.

### Proses Instalasi yang Dapat Disesuaikan

*Installer* CachyOS memungkinkan pengguna untuk menyesuaikan sistem mereka dengan memilih *dekstop environment*, paket, *file-system*, *boot-manager*, kernel, dan lainnya agar sesuai dengan kebutuhan:

- [**Lingkungan Desktop**](/id/installation/desktop_environments/)
- [**Manajer Boot**](/id/installation/boot_managers/)
- [**Varian Kernel**](/id/features/kernel#variants)
- [**Sistem Berkas**](/id/installation/filesystem)
- [**Paket Kustom yang akan disertakan selama instalasi**](https://github.com/CachyOS/cachyos-calamares/blob/cachyos-limine-qt6/src/modules/netinstall/netinstall.yaml)

## Aplikasi CachyOS

CachyOS mengembangkan dan memelihara seperangkat aplikasi miliknya sendiri untuk mempermudah pengelolaan sistem dan meningkatkan pengalaman anda.

Daftar aplikasi yang saat ini dikembangkan dan dikelola oleh CachyOS:

-   **[CachyOS Hello](https://github.com/CachyOS/CachyOS-Welcome):** Aplikasi selamat datang yang mengendalikan pengaturan, memasang perbaikan, dan menginstal paket.
-   **[CachyOS Package Installer](https://github.com/CachyOS/packageinstaller):** Sebuah grafis antarmuka pengguna (GUI) untuk pemasangan aplikasi dengan mudah.
-   **[CachyOS Kernel Manager](https://github.com/CachyOS/kernel-manager):** Dengan mudah memasang kernel dari repositori, konfigurasi kernel dengan mandiri, dan mengelola `sched-ext` *framework*.
-   **[cachyos-rate-mirrors](https://github.com/CachyOS/rate-mirrors):** Secara otomatis mengurutkan Arch and CachyOS *mirrors* untuk mengunduh dengan kecepatan yang optimal dengan `pacman`.
-   **[systemd-boot-manager](https://github.com/CachyOS/systemd-boot-manager):** Secara otomatis membuat entri boot terbaru untuk `systemd-boot`, yang dapat dikonfigurasi dengan mudah lewat `/etc/sdboot-manage.conf`.

## Komunitas yang Ramah dan Aktif

Keunggulan utama CachyOS adalah komunitas yang terus berkembang. Setiap anggota komunitas membantu satu sama lain dengan berbagi tips, memberikan dukungan, dan berkontribusi untuk menyukseskan proyek. Masukkan anda membantu kami untuk terus meningkatkan pengalaman menggunakan CachyOS.

Bergabunglah dengan kami dan menjadi bagian dari komunitas di **[Discord CachyOS](https://discord.com/invite/cachyos-862292009423470592)** dan **[Forum CachyOS](https://discuss.cachyos.org/)**.
