# Analisis Data Panel: Indeks Pembangunan Literasi dan Indeks Pelayanan Publik

Proyek ini melakukan analisis data panel untuk meneliti hubungan antara **Indeks Pembangunan Literasi Masyarakat (IPLM)** sebagai variabel independen (X) dan **Indeks Pelayanan Publik (IPP)** sebagai variabel dependen (Y) di 34 provinsi di Indonesia.

## 📁 Struktur Repository

```
├── Raw Data/
│   ├── Variabel X/          # Data Indeks Pembangunan Literasi Masyarakat
│   │   └── vertikalkementerian-2-od_34152_indeks_pmbngnn_literasi_msyrkt__prov_di_indonesia_v2_data.csv
│   └── Variabel Y/          # Data Indeks Pelayanan Publik
│       └── vertikalkementerian-2-od_34154_indeks_pelayanan_publik__prov_di_indonesia_v1_data.csv
├── Clean Data/
│   └── data_final.csv       # Data gabungan yang sudah dibersihkan
├── Data Cleaning.ipynb      # Notebook untuk preprocessing dan cleaning data
├── Analisis.ipynb           # Notebook untuk analisis statistik dan ekonometrika
└── README.md                # Dokumentasi proyek
```

## 📊 Deskripsi Data

### Variabel X: Indeks Pembangunan Literasi Masyarakat (IPLM)
- **Sumber**: Kementerian Pendidikan, Kebudayaan, Riset, dan Teknologi
- **Periode**: 2020-2024
- **Cakupan**: 34 Provinsi di Indonesia
- **Satuan**: POIN

### Variabel Y: Indeks Pelayanan Publik (IPP)
- **Sumber**: Kementerian Pendayagunaan Aparatur Negara dan Reformasi Birokrasi
- **Periode**: 2021-2024
- **Cakupan**: 34 Provinsi di Indonesia
- **Satuan**: POIN
- **Predikat**: A, A-, B, C (kualitas pelayanan)

### Data Final
Data panel dengan struktur:
- **Entities**: 34 Provinsi
- **Time Periods**: 4 tahun (2021-2024)
- **Total Observasi**: 135

## 🛠️ Teknologi yang Digunakan

- **Python** - Bahasa pemrograman utama
- **pandas** - Manipulasi dan analisis data
- **NumPy** - Komputasi numerik
- **Matplotlib & Seaborn** - Visualisasi data
- **SciPy** - Analisis statistik
- **linearmodels** - Estimasi model data panel (Pooled OLS, Fixed Effects, Random Effects)

## 📝 Alur Kerja

### 1. Data Cleaning (`Data Cleaning.ipynb`)
- Loading dataset dari folder Raw Data
- Eksplorasi struktur data awal
- Pembersihan dan transformasi data
- Penyimpanan hasil ke `Clean Data/data_final.csv`

### 2. Analisis Data (`Analisis.ipynb`)
- Pembentukan struktur data panel
- Statistik deskriptif
- Visualisasi data
- Estimasi model regresi data panel:
  - Pooled OLS
  - Fixed Effects Model
  - Random Effects Model
- Uji asumsi klasik
- Interpretasi hasil

## 🚀 Cara Menjalankan

### Prasyarat
Pastikan Python 3.x sudah terinstall. Install dependencies yang diperlukan:

```bash
pip install pandas numpy matplotlib seaborn scipy linearmodels
```

### Langkah-langkah

1. **Clone repository ini** (jika menggunakan Git):
```bash
git clone <repository-url>
cd <repository-folder>
```

2. **Jalankan Data Cleaning** (opsional, jika ingin memproses ulang data):
```bash
# Buka Data Cleaning.ipynb di Jupyter Notebook atau JupyterLab
jupyter notebook "Data Cleaning.ipynb"
```

3. **Jalankan Analisis**:
```bash
# Buka Analisis.ipynb di Jupyter Notebook atau JupyterLab
jupyter notebook Analisis.ipynb
```

## 📈 Output Analisis

Notebook analisis menghasilkan:
- Statistik deskriptif variabel penelitian
- Visualisasi tren IPP dan IPLM per provinsi
- Hasil estimasi model panel data
- Uji signifikansi koefisien regresi
- Interpretasi pengaruh literasi terhadap kualitas pelayanan publik