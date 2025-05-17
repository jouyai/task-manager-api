Task Manager API
Task Manager API adalah aplikasi backend sederhana yang dibangun menggunakan Node.js, Express, dan MongoDB untuk mengelola tugas (tasks). Aplikasi ini mendukung operasi CRUD (Create, Read, Update, Delete) untuk tugas, memungkinkan pengguna untuk membuat, melihat, memperbarui, dan menghapus tugas melalui RESTful API.
Fitur

Membuat tugas baru dengan judul, deskripsi, dan status.
Melihat semua tugas atau tugas tertentu berdasarkan ID.
Memperbarui tugas yang ada.
Menghapus tugas.
Status tugas dapat berupa: pending, in-progress, atau completed.

Teknologi yang Digunakan

Node.js: Runtime JavaScript untuk backend.
Express: Framework untuk membangun API.
MongoDB: Database NoSQL untuk menyimpan data tugas.
Mongoose: ODM (Object Data Modeling) untuk MongoDB.
dotenv: Untuk mengelola variabel lingkungan.
CORS: Untuk mengizinkan akses lintas domain.

Prasyarat

Node.js (versi 14 atau lebih baru)
MongoDB (lokal atau MongoDB Atlas)
Akun MongoDB Atlas atau server MongoDB lokal yang berjalan
File .env dengan variabel lingkungan yang sesuai

Instalasi

Clone repository:
git clone [text](https://github.com/jouyai/task-manager-api)
cd task-manager-api


Instal dependensi:
npm install


Buat file .env:Buat file .env di root proyek dan tambahkan variabel lingkungan berikut:
PORT=3000
MONGODB_URI=<YOUR_MONGODB_CONNECTION_STRING>

Ganti <YOUR_MONGODB_CONNECTION_STRING> dengan URI MongoDB Anda, misalnya:

Untuk MongoDB lokal: mongodb://localhost:27017/task-manager
Untuk MongoDB Atlas: mongodb+srv://<username>:<password>@cluster0.mongodb.net/task-manager?retryWrites=true&w=majority


Jalankan aplikasi:
node index.js

Server akan berjalan di http://localhost:3000 (atau port lain yang ditentukan di .env).


API Endpoints



Method
Endpoint
Deskripsi
Body (JSON)



GET
/api/tasks
Mengambil semua tugas
-


GET
/api/tasks/:id
Mengambil tugas berdasarkan ID
-


POST
/api/tasks
Membuat tugas baru
{ "title": "string", "description": "string", "status": "pending/in-progress/completed" }


PUT
/api/tasks/:id
Memperbarui tugas
{ "title": "string", "description": "string", "status": "pending/in-progress/completed" }


DELETE
/api/tasks/:id
Menghapus tugas
-


Contoh Request

Membuat tugas:
curl -X POST http://localhost:3000/api/tasks -H "Content-Type: application/json" -d '{"title":"Belajar Node.js","description":"Mempelajari Express dan MongoDB","status":"pending"}'


Mengambil semua tugas:
curl http://localhost:3000/api/tasks



Struktur Proyek
task-manager-api/
├── node_modules/
├── .env
├── .gitignore
├── index.js
├── package.json
└── README.md

Catatan

Pastikan MongoDB berjalan sebelum menjalankan aplikasi.
Gunakan alat seperti Postman atau Insomnia untuk menguji endpoint API.
File .env harus ditambahkan ke .gitignore untuk mencegah pengunggahan informasi sensitif ke repository.

Kontribusi

Fork repository ini.
Buat branch baru (git checkout -b feature/nama-fitur).
Commit perubahan (git commit -m 'Menambahkan fitur X').
Push ke branch (git push origin feature/nama-fitur).
Buat Pull Request.

Lisensi
Proyek ini dilisensikan di bawah MIT License.
