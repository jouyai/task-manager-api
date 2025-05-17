# Task Manager API

Task Manager API adalah aplikasi backend berbasis **Node.js**, **Express**, dan **MongoDB** untuk mengelola tugas dengan operasi CRUD (Create, Read, Update, Delete). Aplikasi ini memungkinkan pengguna untuk membuat, melihat, memperbarui, dan menghapus tugas melalui RESTful API.

## Fitur
- Membuat tugas baru dengan judul, deskripsi, dan status (`pending`, `in-progress`, `completed`).
- Melihat semua tugas atau tugas tertentu berdasarkan ID.
- Memperbarui informasi tugas.
- Menghapus tugas.

## Teknologi yang Digunakan
- **Node.js**: Runtime untuk backend.
- **Express**: Framework untuk API.
- **MongoDB**: Database NoSQL.
- **Mongoose**: ODM untuk MongoDB.
- **dotenv**: Mengelola variabel lingkungan.
- **CORS**: Mendukung akses lintas domain.

## Prasyarat
- Node.js (versi 14 atau lebih baru)
- MongoDB (lokal atau MongoDB Atlas)
- File `.env` dengan variabel lingkungan

## Instalasi
1. Clone repository:
   ```bash
   git clone https://github.com/jouyai/task-manager-api.git
   cd task-manager-api
2. Install dependensi:
   ```bash
   npm install
2. Buat file .env di root proyek dan tambahkan:
   ```bash
   PORT=3000
   MONGODB_URI=<YOUR_MONGODB_CONNECTION_STRING>
3. Jalankan Aplikasi:
   ```bash
   npm start