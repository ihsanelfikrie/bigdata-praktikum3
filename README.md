# 🚀 Big Data Technology — Praktikum 3
## Batch Data Analytics + Visualization Layer
### Big Data Dashboard (Microsoft Power BI)

![Python](https://img.shields.io/badge/Python-3.12-blue?logo=python)
![PySpark](https://img.shields.io/badge/PySpark-3.x-orange?logo=apache-spark)
![Power BI](https://img.shields.io/badge/Power%20BI-Dashboard-yellow?logo=powerbi)
![Ubuntu](https://img.shields.io/badge/Ubuntu-WSL2-purple?logo=ubuntu)

---

## 👤 Identitas Mahasiswa

| | |
|---|---|
| **Nama** | Muhammad Nur Ihsan |
| **NIM** | 230104040214 |
| **Program Studi** | Teknologi Informasi |
| **Universitas** | UIN Antasari |
| **Mata Kuliah** | Big Data Technology |
| **Dosen** | Muhayat, M.IT |
| **Tahun** | 2026 |

---

## 📋 Deskripsi Praktikum

Praktikum 3 berfokus pada pembuatan **Batch Data Analytics Pipeline** lengkap dari raw data hingga visualisasi dashboard interaktif menggunakan Power BI. Pipeline ini mensimulasikan arsitektur Big Data modern yang digunakan di industri.

---

## 🏗️ Arsitektur Pipeline

```
Raw Dataset (CSV)
       ↓
Spark Processing (clean_data.py)
       ↓
Clean Data (Parquet)
       ↓
Analytics Layer (analytics_layer.py)
       ↓
Serving Layer (CSV)
       ↓
Power BI Dashboard
```

---

## 🛠️ Teknologi yang Digunakan

| Teknologi | Versi | Fungsi |
|-----------|-------|--------|
| Python | 3.12 | Bahasa pemrograman utama |
| PySpark | 3.x | Distributed data processing |
| Pandas | Latest | Data manipulation |
| Matplotlib | Latest | Visualisasi chart |
| Power BI Desktop | Latest | Business Intelligence Dashboard |
| Ubuntu (WSL2) | 24.04 | Linux environment di Windows |
| Java OpenJDK | 17 | Runtime untuk PySpark |
| VS Code | Latest | Code editor |

---

## 📁 Struktur Project

```
bigdata_project/
├── data/
│   ├── raw/
│   │   └── ecommerce.csv          # Dataset mentah e-commerce
│   ├── clean/
│   │   └── parquet/               # Clean data (Silver Layer)
│   └── serving/
│       ├── total_revenue/         # KPI: Total Revenue
│       ├── top_products/          # KPI: Top 10 Products
│       ├── category_revenue/      # KPI: Revenue per Category
│       └── avg_transaction/       # KPI: Avg Transaction Value
├── scripts/
│   ├── clean_data.py              # Script cleaning data dengan Spark
│   ├── analytics_layer.py         # Script analytics & KPI
│   └── visualization_layer.py     # Script visualisasi Matplotlib
├── reports/
│   ├── bigdata_dashboard.pbix     # File Power BI Dashboard
│   ├── category_revenue.png       # Chart revenue per kategori
│   ├── top_products.png           # Chart top products
│   ├── total_revenue.csv          # Export KPI total revenue
│   ├── top_products.csv           # Export KPI top products
│   └── category_revenue.csv       # Export KPI category revenue
├── venv/                          # Virtual environment Python
└── README.md                      # Dokumentasi project
```

---

## ⚙️ Cara Menjalankan Project

### 1. Prerequisites

Pastikan sudah terinstall:
- Windows 11 dengan WSL2 (Ubuntu 24.04)
- Python 3.12
- Java OpenJDK 17
- VS Code

### 2. Clone Repository

```bash
git clone https://github.com/ihsanelfikrie/bigdata-praktikum3.git
cd bigdata-praktikum3
```

### 3. Setup Virtual Environment

```bash
python3 -m venv venv
source venv/bin/activate
```

### 4. Install Dependencies

```bash
pip install pyspark pandas matplotlib
```

### 5. Jalankan Pipeline

```bash
# Step 1: Clean Data
python scripts/clean_data.py

# Step 2: Analytics Layer
python scripts/analytics_layer.py

# Step 3: Visualization
python scripts/visualization_layer.py
```

---

## 📊 KPI yang Dihasilkan

| KPI | Nilai | Keterangan |
|-----|-------|-----------|
| **Total Revenue** | Rp 23.650.000 | Total pendapatan keseluruhan |
| **Top Product** | Buku ML | Produk terlaris berdasarkan quantity |
| **Kategori Terbesar** | Electronics | Revenue Rp 18.350.000 |
| **Total Transaksi** | 20 | Total data transaksi |

---

## 📈 Hasil Dashboard Power BI

Dashboard mencakup:
- ✅ **KPI Card** — Total Revenue (Rp 23.650.000)
- ✅ **Bar Chart** — Top Products by Quantity
- ✅ **Bar Chart** — Revenue per Category
- ✅ **Judul** — E-Commerce Sales Dashboard

---

## 🔑 Penjelasan Script

### clean_data.py
Script ini membaca raw CSV menggunakan PySpark, membersihkan data (menghapus null, filter data tidak valid), dan menyimpan hasilnya dalam format Parquet (Silver Layer).

### analytics_layer.py
Script ini membaca clean data dari Parquet, menghitung 4 KPI utama (Total Revenue, Top Products, Revenue per Category, Avg Transaction), dan menyimpan hasilnya sebagai CSV di Serving Layer.

### visualization_layer.py
Script ini membaca clean data dan menghasilkan chart PNG menggunakan Matplotlib untuk Revenue per Category dan Top Products.

---

## 💡 Insight Praktikum

> **Power BI tidak memproses Big Data secara langsung.**
> Proses utama dilakukan oleh **PySpark di Spark Processing Layer**.
> Power BI hanya menampilkan hasil analisis dalam bentuk dashboard
> interaktif untuk membantu pengambilan keputusan bisnis.

---

## 📚 Referensi

- [Apache Spark Documentation](https://spark.apache.org/docs/latest/)
- [PySpark Documentation](https://spark.apache.org/docs/latest/api/python/)
- [Power BI Documentation](https://docs.microsoft.com/power-bi/)
- Modul Praktikum Big Data Technology — UIN Antasari 2026

---

*Muhammad Nur Ihsan — NIM 230104040214 — UIN Antasari 2026*
