# BLUEPRINT CIPTA_DAUN_MAS

<h1 align="center">🍂 Cipta Daun Mas — "The King of Tobacco"</h1>
<p align="center"><i>Aplikasi Mobile Manajemen Katalog dan Transaksi Pemesanan Tembakau Premium Madura</i></p>

---

## 📖 Deskripsi Proyek
**Cipta Daun Mas** adalah platform aplikasi mobile eksklusif yang dirancang untuk mendigitalkan portofolio, edukasi, dan transaksi produk tembakau berkualitas tinggi dari Tanah Madura. Dibangun menggunakan framework Flutter, aplikasi ini mengusung antarmuka bertema *Luxury-Dark* untuk menonjolkan kesan elegan, premium, dan berwibawa. Aplikasi ini berfungsi sebagai jembatan langsung (*Direct-to-Admin*) antara konsumen dan gudang tanpa perantara.

## ✨ Fitur Unggulan (Core Features)
1. **Katalog Digital Interaktif:** Menyajikan 15 variasi tembakau nusantara (seperti Rajangan Pamekasan, Prancak 95, Srintil, hingga Kasturi Jember) yang terstruktur rapi menggunakan arsitektur *Sliver Grid*, lengkap dengan informasi harga dan sisa stok.
2. **Direct WhatsApp Gateway (Automated Ordering):** Sistem transaksi cerdas yang mengenkripsi data pemesanan pelanggan (berdasarkan nama varian produk) dan meneruskannya secara otomatis ke ruang obrolan WhatsApp Admin menggunakan dependensi `url_launcher`.
3. **Offline-First Asset Management:** Sepenuhnya menggunakan manajemen *Local Assets* untuk pemuatan seluruh 19 foto resolusi tinggi secara instan. Menjamin aplikasi tetap super ringan, bebas *lag*, dan gambar tidak akan hilang meskipun tanpa koneksi internet.
4. **Live Market Trend Chart:** Visualisasi grafik garis (*Line Chart*) tren harga harian yang digambar langsung oleh mesin aplikasi menggunakan *CustomPainter*, bukan gambar statis.
5. **Dynamic Marquee Announcement:** Fitur *running text* otomatis di halaman beranda untuk menyiarkan informasi pergerakan stok dan ekspor secara *real-time*.

## 🎨 Identitas Visual (UI/UX)
Sistem pewarnaan aplikasi telah distandarisasi untuk menjaga konsistensi identitas merek:
* **Background Surface (`#121414`):** Hitam pekat untuk aksentuasi *dark-mode* premium.
* **Primary Gold (`#D7942D`):** Emas elegan yang merepresentasikan kualitas daun tembakau.
* **Surface Container (`#1E2020`):** Abu-abu gelap untuk memisahkan batas elemen kartu dengan latar.
* **Outline & Text (`#9E8E7C` & `#E2E2E2`):** Cokelat redup dan putih terang demi visibilitas pembacaan (*readability*) yang maksimal.

## ⚙️ Stack Teknologi & Arsitektur
* **Framework:** Flutter SDK
* **Bahasa Pemrograman:** Dart (Strict Typing)
* **Arsitektur:** Modular Component-Based (Stateful & Stateless Widgets)
* **Rendering Engine:** Skia / Impeller Custom Paint
* **Version Control:** Git / GitHub
* **IDE:** Visual Studio Code (VS Code)

## 🗂️ Struktur Direktori & Modul
```text
cipta_daun_mas/
├── android/app/src/main/AndroidManifest.xml  # Konfigurasi perizinan akses Intent (URL Skema)
├── assets/images/                            # Brankas Aset Gambar Lokal (Rasio 1:1, max 150KB)
│   ├── a0.jpg, a1.jpg, a2.jpg                # Foto Katalog Beranda (Koleksi Premium)
│   ├── produk1.jpg s/d produk15.jpg          # Foto 15 Varian Tembakau
│   └── owner.jpg                             # Foto Profil Eksekutif
├── lib/
│   ├── pages/
│   │   ├── beranda_page.dart                 # Modul Dashboard & Analisis Harga
│   │   ├── katalog_page.dart                 # Modul Grid Produk & Engine Pemesanan WA
│   │   ├── edukasi_page.dart                 # Modul Informasi Teknis Pengolahan
│   │   └── profil_page.dart                  # Modul Legalitas & Operasional Gudang
│   └── main.dart                             # Entry Point & Global Navigation Route
└── pubspec.yaml                              # Registrasi Assets & Dependensi Pihak Ketiga

