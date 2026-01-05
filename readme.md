# ☕ Ngofee POS - Point of Sales System

**Ngofee POS** adalah aplikasi berbasis web untuk manajemen pemesanan minuman di kedai kopi. Aplikasi ini dirancang menggunakan arsitektur Microservices sederhana, terkontainerisasi dengan Docker, dan terintegrasi dengan layanan eksternal untuk menampilkan info event/konser.

Project ini disusun untuk memenuhi **Tugas Besar / UAS Teknologi Sistem Terdistribusi**.

## 👥 Anggota Kelompok
* **Valereo Jibril Al Buchori** (18223030) - *Core Service Developer (POS)*
* **Mahesa Satria Prayata** (18223082) - *Partner & Integration Service Developer*

---

## 🚀 Fitur Utama

1.  **Katalog Minuman**: Menampilkan daftar menu kopi dan non-kopi dengan harga dan gambar.
2.  **Top Sellers**: Algoritma untuk menampilkan produk terlaris/termahal di halaman utama.
3.  **Pencarian**: Fitur *live search* untuk mencari menu dengan cepat.
4.  **Manajemen Keranjang**: Menambah, mengurangi, dan menghapus item sebelum checkout.
5.  **Autentikasi User**:
    * Registrasi & Login pengguna (Hashing password dengan Bcrypt).
    * Keamanan transaksi menggunakan **JWT (JSON Web Token)**.
6.  **Integrasi Layanan Eksternal (Service Mahesa)**:
    * Aplikasi secara otomatis mengambil data jadwal konser dari API partner.
    * Jika ada konser di *venue* tertentu (misal: PIA ARENA MM), banner aplikasi akan berubah menjadi tema konser secara dinamis.

---

## 🛠️ Teknologi yang Digunakan

* **Backend**: Node.js, Express.js
* **Database**: PostgreSQL (Cloud via Neon DB)
* **Frontend**: HTML5, CSS3, Vanilla JavaScript (Single Page Application logic)
* **Containerization**: Docker & Docker Compose
* **Security**: BCryptJS, JWT, CORS

---

## 📂 Struktur Project

```text
.
├── config/             # Konfigurasi Database (PostgreSQL)
├── controllers/        # Logika bisnis (Auth & Drink Controller)
├── public/             # Frontend Static Files (HTML, CSS, JS)
├── routes/             # Definisi Endpoint API
├── .env                # Environment Variables (Tidak di-upload ke git)
├── docker-compose.yml  # Orkestrasi Container
├── Dockerfile          # Image Build Instruction
├── server.js           # Entry Point Aplikasi
└── package.json        # Dependencies Node.js
