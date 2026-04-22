# Simple Agent Skills with Bookstore App

Proyek ini adalah repositori untuk belajar tentang **Agent Skills** menggunakan kerangka kerja [Pi Coding Agent](https://github.com/mariozechner/pi-coding-agent), sekaligus mengimplementasikan aplikasi backend sederhana (Bookstore API) menggunakan **FastAPI**.

## 🚀 Fitur

1. **Bookstore API**: Aplikasi FastAPI sederhana dengan endpoint untuk melihat dan menambahkan buku.
2. **Agent Skills Playground**: Proyek ini memiliki folder `.pi/skills` yang memuat custom agent skills yang sedang dipelajari/dikembangkan.

## 🛠️ Stack Teknologi

- **Python** (>= 3.14)
- **FastAPI** (Web Framework)
- **Uvicorn** (ASGI server)
- **uv** (Package manager)
- **Pi Coding Agent** (Untuk Agent Skills)

## 📂 Struktur Proyek

```text
.
├── .pi/
│   └── skills/           # Direktori tempat Agent Skills disimpan
│       ├── my-skill/
│       └── pr-description/
├── main.py               # Source code aplikasi FastAPI Bookstore
├── pyproject.toml        # Konfigurasi project & dependensi Python
├── uv.lock               # Lockfile untuk dependensi (uv)
└── README.md
```

## ⚙️ Cara Menjalankan Aplikasi

Proyek ini menggunakan `uv` untuk manajemen dependensi.

1. **Instalasi Dependensi**
   Pastikan Anda sudah menginstal `uv`, kemudian jalankan:
   ```bash
   uv sync
   ```

2. **Menjalankan Server (FastAPI)**
   Jalankan uvicorn server dengan perintah:
   ```bash
   uv run uvicorn main:app --reload
   ```
   Aplikasi akan berjalan di `http://127.0.0.1:8000`.

3. **Melihat Dokumentasi API**
   Buka browser dan arahkan ke:
   - Swagger UI: `http://127.0.0.1:8000/docs`
   - ReDoc: `http://127.0.0.1:8000/redoc`

### Endpoint yang Tersedia

- `GET /books` : Mengambil daftar semua buku (mendukung query `?limit=N`).
- `GET /books/{book_id}` : Mengambil data buku spesifik berdasarkan ID.
- `POST /books` : Menambahkan buku baru.

## 🤖 Tentang Agent Skills

Di repositori ini, Anda akan menemukan direktori `.pi/skills/` yang berisi skill kustom untuk Pi Coding Agent.
Skill yang telah dibuat:
- `my-skill`: Skill eksperimen/contoh awal.
- `pr-description`: Skill yang dirancang untuk membantu membuat deskripsi Pull Request secara otomatis.

Agent akan secara otomatis mengenali folder-folder di dalam `.pi/skills/` ini berkat file `SKILL.md` yang ada di dalamnya.
