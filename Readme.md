## 📁 Struktur Folder

```
ssti-flask/
├── app.py
├── requirements.txt
└── README.md
```

---

# 🔒 SSTI Vulnerability Demo using Python Flask

Repositori ini berisi simulasi eksploitasi *Server-Side Template Injection (SSTI)* menggunakan Python Flask. Tujuan dari repositori ini adalah edukatif, untuk memahami bagaimana SSTI terjadi dan bagaimana mencegahnya.

## 📚 Deskripsi Singkat

**SSTI (Server-Side Template Injection)** terjadi ketika input pengguna dimasukkan ke dalam template engine tanpa filter yang aman, memungkinkan eksekusi kode berbahaya di sisi server.

Artikel lengkap dapat dibaca di:  
🔗 [https://fauxies.blogspot.com/2025/05/server-side-template-injection.html](https://fauxies.blogspot.com/2025/05/server-side-template-injection.html)

## ⚠️ PERINGATAN

> **Simulasi ini hanya untuk tujuan pembelajaran dan dilakukan di lingkungan lokal. Jangan pernah digunakan pada server produksi.**

---

## 📦 Instalasi

### 1. Clone Repository

```bash
git clone https://github.com/FadzarSuryaWijaya/ssti
cd ssti
````

### 2. Buat Virtual Environment (Opsional)

```bash
python -m venv venv
source venv/bin/activate    # Mac/Linux
venv\Scripts\activate       # Windows
```

### 3. Install Dependensi

```bash
pip install -r requirements.txt
```

---

## ▶️ Menjalankan Aplikasi

```bash
python app.py
```

Aplikasi akan berjalan di `http://127.0.0.1:5000/`

---

## 🧪 Contoh Eksploitasi SSTI

Buka browser dan coba akses:

```
http://127.0.0.1:5000/?name={{7*7}}
```

Jika muncul `Hello 49`, maka aplikasi berhasil dieksploitasi via SSTI.

---

## ✅ Cara Mencegah SSTI

1. Jangan pernah menyisipkan input langsung ke dalam template.
2. Gunakan `render_template()` bukan `render_template_string()`.
3. Validasi input dengan ketat.
4. Gunakan sandbox template engine.
5. Cek log aktivitas untuk mendeteksi payload aneh (`{{`, `${`, `<%`, dsb).
6. Lakukan pentest keamanan secara berkala.

---

## 📚 Referensi

* [OWASP - Server-Side Template Injection](https://owasp.org/www-project-web-security-testing-guide/)
* [PortSwigger Academy - SSTI](https://portswigger.net/web-security/server-side-template-injection)

---

## 📄 Lisensi

MIT License – Gunakan dengan bijak.

---

## 🧑‍🎓 Disusun Oleh

**Fadzar Surya Wijaya**
NIM: 312310451
Universitas Pelita Bangsa
2025

````

---

### ✅ Langkah Selanjutnya

1. Simpan ketiga file (`app.py`, `requirements.txt`, `README.md`) dalam satu folder.
2. Inisialisasi git repo dan upload ke GitHub:

```bash
git init
git add .
git commit -m "Initial commit - Demo SSTI Flask"
git remote add origin https://github.com/FadzarSuryaWijaya/ssti
git push -u origin master
````

