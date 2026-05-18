cat << 'EOF' > README.md
# 🚀 X-Channel Bridge API Documentation

Dokumentasi resmi integrasi API Gateway untuk pengecekan data operator otomatis (*Cek Sidompul*). API ini dilengkapi dengan sistem pengecekan kredensial, deteksi *prefix* otomatis, dan auto-cut saldo.

---

## 📌 Base URL
* **Development / Local:** `http://localhost:17500`
* **Production:** `http://xchannell.web.id`

---

## 🛠️ API Reference

### 1. Cek Sidompul (Otomatis)
Endpoint ini digunakan untuk mengecek status dompul berdasarkan nomor HP. Sistem backend akan mendeteksi operator (XL, Axis, Tri, Indosat) secara otomatis berdasarkan 4 digit pertama (*prefix*) nomor telepon. User tidak perlu mengirimkan parameter operator.

* **URL:** `/api/tools/cek-sidompul`
* **Method:** `POST`
* **Headers:**
  ```http
  Content-Type: application/json

