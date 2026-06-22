# 🛒 E-Commerce Sentiment Analysis Agent

AI Agent berbasis LangFlow untuk analisis otomatis ulasan produk e-commerce — mencakup summarization, sentiment analysis, dan rekomendasi strategis berbasis data pelanggan.

---

## 📌 Problem Statement

Tim produk dan pengambil keputusan di platform e-commerce seringkali kesulitan memproses ribuan ulasan pelanggan secara manual. Volume data yang besar menyebabkan insight penting sering terlewat, analisis menjadi lambat, dan rekomendasi perbaikan produk tidak berbasis data yang akurat.

---

## 🎯 Target Users

- Product Manager & Tim Produk E-Commerce
- Business Analyst
- Pengambil keputusan bisnis yang membutuhkan insight cepat dari ulasan pelanggan

---

## ✨ Fitur Utama

- **Summarization** — Merangkum ratusan ulasan menjadi narasi ringkas dan informatif
- **Sentiment Analysis** — Mengklasifikasikan sentimen dominan pelanggan (Positive / Neutral / Negative)
- **Strategic Recommendations** — Menghasilkan action items terstruktur berdasarkan pola ulasan
- **Priority-based Action Items** — Rekomendasi diurutkan berdasarkan dampak (High / Medium / Low)

---

## 🔄 Alur Sistem

```
Input: Data Ulasan Produk (CSV)
        ↓
Prompt Template 1
→ Summarization + Sentiment Analysis + Average Rating + Dominant Theme
        ↓
Prompt Template 2
→ Strategic Recommendations + Action Items (Priority, Area, Issue, Recommendation, Expected Impact)
        ↓
Output: Laporan Analisis Siap Pakai
```

---

## 🛠️ Tech Stack

- **LangFlow** — AI Agent workflow builder
- **Docker** — Environment untuk menjalankan LangFlow
- **IBM Watsonx / OpenAI** — LLM backend

---

## 📁 Struktur Folder

```
ecommerce-sentiment-analysis-agent/
├── flow/
│   └── sentiment_analysis_agent.json   # Export flow LangFlow
├── data/
│   └── sample_reviews.csv              # Sample dataset (data dummy)
├── docs/
│   └── Capstone_Project.docx           # Dokumentasi proyek
└── README.md
```

---

## 📊 Dataset

> ⚠️ Dataset asli bersifat confidential dan tidak disertakan dalam repository ini.
> File `sample_reviews.csv` merupakan data dummy dengan struktur yang sama untuk keperluan demonstrasi.

### Struktur Dataset

| Kolom | Tipe | Keterangan |
|---|---|---|
| message_id | integer | ID unik untuk setiap ulasan |
| Product_name | string | Nama produk yang diulas |
| Review | string | Isi ulasan dari pelanggan |
| Rating | integer | Rating numerik skala 1–5 |

---

## 🚀 Cara Menjalankan

1. **Clone repository ini**
   ```bash
   git clone https://github.com/username/ecommerce-sentiment-analysis-agent.git
   ```

2. **Jalankan LangFlow via Docker**
   ```bash
   docker run -p 7860:7860 langflowai/langflow
   ```

3. **Import flow ke LangFlow**
   - Buka `http://localhost:7860`
   - Klik **Import** → pilih file `flow/sentiment_analysis_agent.json`

4. **Siapkan dataset**
   - Gunakan `data/sample_reviews.csv` sebagai contoh
   - Atau ganti dengan dataset Anda sendiri dengan struktur yang sama

5. **Jalankan Agent**
   - Masukkan data ulasan ke input
   - Klik **Run** dan lihat hasilnya

---

## 💡 Potensi Pengembangan

- Analisis tren sentimen berbasis waktu (time-series sentiment tracking)
- Perbandingan otomatis antar produk secara bersamaan
- Integrasi dashboard visualisasi real-time
- Dukungan analisis ulasan multibahasa secara otomatis

---

## 👤 Author

Dibuat sebagai bagian dari **IBM SkillsBuild x Hacktiv8 AI Agent Training — Capstone Project**

---

## 📄 License

MIT License — bebas digunakan dengan mencantumkan kredit kepada pembuat asli.
