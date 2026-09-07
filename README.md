# Warung Kentang — Website Marketplace Kentang Goreng

Website satu halaman (single-page) untuk menampilkan 4 menu kentang goreng, lengkap dengan keranjang belanja dan tombol pesan via WhatsApp. Tidak butuh server atau database — cukup file statis (HTML, CSS, JS) sehingga bisa langsung dihosting **gratis** lewat GitHub Pages.

## Isi folder

```
kentang-store/
├── index.html          -> halaman utama (semua CSS & JS sudah menyatu di sini)
├── images/
│   ├── tomat.jpg        -> Kentang Goreng (Saus Tomat)
│   ├── mayo.jpg         -> Kentang Goreng (Saus Mayo)
│   ├── keju.jpg         -> Kentang Goreng (Keju)
│   └── keriting.jpg     -> Kentang Goreng (Keriting)
└── README.md            -> file ini
```

## Cara upload ke GitHub agar dapat domain gratis

1. **Buat akun GitHub** (jika belum punya) di https://github.com

2. **Buat repository baru**
   - Klik tombol **New** di halaman github.com
   - Beri nama repository, misalnya `warung-kentang`
   - Pilih **Public**
   - Klik **Create repository**

3. **Upload file ke repository**
   - Di halaman repository yang baru dibuat, klik **Add file > Upload files**
   - Seret (drag & drop) seluruh isi folder `kentang-store` (index.html, folder images, README.md) ke area upload
   - Pastikan struktur foldernya tetap sama — folder `images` harus tetap bernama `images`
   - Klik **Commit changes**

4. **Aktifkan GitHub Pages**
   - Buka tab **Settings** pada repository
   - Di menu sebelah kiri, pilih **Pages**
   - Pada bagian **Source**, pilih branch **main** dan folder **/ (root)**
   - Klik **Save**

5. **Tunggu 1–2 menit**, lalu refresh halaman Settings > Pages. GitHub akan menampilkan alamat website kamu, biasanya berbentuk:

   ```
   https://<username-github-kamu>.github.io/warung-kentang/
   ```

   Itulah domain gratis untuk website kamu.

## Cara mengubah isi website

- **Ganti nomor WhatsApp**: buka `index.html`, cari baris:
  ```js
  const WHATSAPP_NUMBER = "6281234567890";
  ```
  Ganti dengan nomor WhatsApp toko kamu (format: kode negara tanpa tanda `+`, contoh nomor Indonesia diawali `62`).

- **Ganti harga atau nama menu**: masih di `index.html`, cari bagian `PRODUCTS = [ ... ]` dan ubah nilai `name`, `desc`, atau `price` sesuai kebutuhan.

- **Ganti foto produk**: ganti file di dalam folder `images/` dengan nama file yang sama (`tomat.jpg`, `mayo.jpg`, `keju.jpg`, `keriting.jpg`), atau ubah nama file di `PRODUCTS` agar sesuai foto baru.

## Catatan

- Semua transaksi diarahkan ke WhatsApp — tidak ada pembayaran online otomatis di dalam halaman ini.
- Keranjang belanja tersimpan di browser pengunjung (localStorage), jadi tidak akan hilang walau halaman ditutup, tapi juga tidak tersinkron ke perangkat lain.
