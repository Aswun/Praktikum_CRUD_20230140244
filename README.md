# Dokumentasi API Manajemen Pengguna - Praktikum CRUD

Repositon ini berisi implementasi API untuk mengelola data pengguna (User) menggunakan Spring Boot.

## Konfigurasi Akses

Akses ke seluruh layanan API dilakukan melalui alamat dasar (Base URL) berikut:
`http://localhost:8080/api/users`

---

## Fitur dan Endpoint

### 1. Registrasi Pengguna Baru (Create)

Fungsi ini digunakan untuk menambahkan data user ke sistem. ID akan di-generate secara otomatis menggunakan format UUID.

<img width="1920" height="1200" alt="image" src="https://github.com/user-attachments/assets/9f1e975f-77b6-4f4d-bcef-8ea7df1e042f" />

* **Metode:** `POST`
* **Alamat:** `/api/users`
* **Format Data:** `application/json`

**Contoh Request Body:**

```json
{
  "name": "Aswun",
  "age": 21
}

```

---

### 2. Menampilkan Seluruh Daftar User (Read)

Digunakan untuk mengambil semua data pengguna yang tersimpan dalam database.

<img width="1920" height="1200" alt="image" src="https://github.com/user-attachments/assets/3bf84fb3-247d-4d22-8424-ded3e80fb4f7" />

* **Metode:** `GET`
* **Alamat:** `/api/users`

**Struktur Respon Sukses:**

```json
{
    "status": "success",
    "data": [
        {
            "id": "uuid-string-otomatis",
            "name": "Aswun",
            "age": 21
        }
    ]
}

```

---

### 3. Memperbarui Informasi User (Update)

Melakukan perubahan data pada user yang sudah ada berdasarkan ID yang spesifik.

<img width="1920" height="1200" alt="image" src="https://github.com/user-attachments/assets/24c611dc-56a7-4cac-8ae1-2b87ba22ab82" />

* **Metode:** `PUT`
* **Alamat:** `/api/users/{id}`

---

### 4. Menghapus Data User (Delete)

Menghapus record pengguna secara permanen dari sistem berdasarkan parameter ID.

<img width="1920" height="1200" alt="image" src="https://github.com/user-attachments/assets/2b22af72-d349-49a6-acd8-67d50a3a4a54)" />

* **Metode:** `DELETE`
* **Alamat:** `/api/users/{id}`

---

## Lampiran Tampilan Sistem

### Antarmuka Web (Frontend)

Berikut adalah tampilan halaman manajemen user saat diakses melalui browser:
<<img width="1920" height="1200" alt="image" src="https://github.com/user-attachments/assets/06a4a043-617a-4e10-adbb-aad879861117" />

### Struktur Database (MySQL)

Representasi data yang tersimpan pada tabel `users` di database:
<img width="1920" height="1200" alt="image" src="https://github.com/user-attachments/assets/aa8e558b-ad34-4301-8a3c-ff01a80677e7"/>
