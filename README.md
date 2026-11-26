# Proyek 7 — Benchmarking Performa Sistem Operasi (Linux vs Windows)

Repositori Kelompok 1, Kelas C — Mata Kuliah Sistem Operasi.

## Tujuan
Menganalisis dan membandingkan performa CPU, RAM, dan disk pada Debian Linux dan Windows 11 melalui pengujian benchmark/stress test, pencatatan hasil, grafik, dan laporan analisis.

## Anggota Kelompok

| No. | Nama | NIM | Tanggung jawab utama |
|---:|---|---|---|
| 1 | Fikri Restu Nugraha | 2501020109 | Ketua / Koordinator |
| 2 | Virtuando Jagad Saputrana | 2501020106 | System Analyst |
| 3 | Almand Zaky. S | 2501020114 | Linux Engineer |
| 4 | Yazira Sartika | 2501020103 | Data Analyst & Dokumentasi |
| 5 | Raihan Parsa | 2501020104 | Windows Engineer |

## Ruang Lingkup

- Sistem operasi yang dibandingkan: Debian Linux dan Windows 11.
- Komponen: CPU, RAM, dan media penyimpanan (disk).
- Tools yang direncanakan: Sysbench, FIO, dan Stress-ng, dengan pemilihan berdasarkan kompatibilitas dan fungsi masing-masing.
- Pengujian utama diutamakan pada perangkat keras nyata. Hasil VirtualBox harus diberi label dan dianalisis terpisah dari hasil native.
- Perbandingan Debian dan Windows pada perangkat yang sama lebih diutamakan agar pengaruh perbedaan hardware dapat dikendalikan.
- Setiap hasil harus menyimpan identitas perangkat, OS, versi tool, konfigurasi, satuan, dan nomor pengulangan.

## Struktur Folder

```text
.
├── README.md
├── .gitignore
├── docs/
│   ├── proposal/
│   ├── laporan-akhir/
│   └── referensi/
├── benchmark/
│   ├── debian/
│   ├── windows/
│   ├── konfigurasi/
│   └── scripts/
├── data/
│   ├── mentah/
│   ├── olahan/
│   └── templat/
├── analisis/
├── bukti-pengujian/
│   └── screenshot/
└── presentasi/
```

## Alur Kerja

1. Menyelesaikan proposal dan menetapkan metode pengujian.
2. Menginventarisasi perangkat serta memastikan metode instalasi OS (native atau virtual).
3. Memasang dan memverifikasi tools benchmark pada lingkungan yang digunakan.
4. Menjalankan benchmark CPU dan RAM.
5. Menjalankan benchmark disk dengan file uji khusus, bukan perangkat/partisi mentah.
6. Mengulang skenario secara konsisten dan menyimpan semua hasil mentah.
7. Mengolah data, membuat grafik, dan menyusun analisis.
8. Menyelesaikan laporan, dokumentasi, dan presentasi.

## Catatan Metodologi

- Jangan membandingkan hasil Debian native dengan Windows yang berjalan di VirtualBox/WSL seolah-olah kondisinya setara.
- Catat model CPU, core/thread, kapasitas RAM, model/jenis/kapasitas storage, versi OS, mode daya, tool dan versinya.
- Gunakan workload, ukuran data, durasi, dan parameter yang sama jika tool mendukung kedua OS.
- Lakukan pengulangan (rencana awal minimal tiga kali) dan laporkan nilai rata-rata serta variasinya.
- Sysbench tidak digunakan sebagai perbandingan native Windows apabila hanya berjalan melalui lingkungan kompatibilitas seperti WSL. Pilih benchmark lintas platform yang setara untuk perbandingan utama CPU/RAM.
- Stress-ng digunakan untuk stress testing dan observasi respons sistem, bukan dianggap sebagai skor benchmark presisi.
- Untuk FIO, gunakan file uji khusus di folder kerja. Jangan mengarahkan pengujian ke raw disk atau partisi sistem.
- Simpan konfigurasi dan log yang dipakai agar pengujian dapat diulang.

## Status
Repositori ini merupakan kerangka awal. Isi proposal, konfigurasi final, data pengujian, grafik, dan laporan akan ditambahkan setelah disiapkan dan diverifikasi oleh kelompok.

## Referensi Teknis

- [Debian Documentation](https://www.debian.org/doc/)
- [FIO Documentation](https://fio.readthedocs.io/)
- [Sysbench](https://github.com/akopytov/sysbench)
- [Stress-ng](https://github.com/ColinIanKing/stress-ng)
- [Phoronix Test Suite](https://www.phoronix-test-suite.com/)
