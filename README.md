
# Penerapan Case-Based Reasoning (CBR) untuk Klasifikasi Kasus Narkotika dan Psikotropika pada Pengadilan Negeri Kandangan

Proyek ini menggunakan metode Case-Based Reasoning (CBR) untuk mengklasifikasikan kasus hukum pada Pengadilan Negeri Kandangan, khususnya kategori **Pidana Khusus > Narkotika dan Psikotropika**, berdasarkan data yang diperoleh dari situs Direktori Putusan Mahkamah Agung Republik Indonesia.

## 📁 Struktur Direktori

```
.
├── data/               # Berisi dataset mentah & hasil preprocessing
├── notebooks/          # Berisi Jupyter Notebook per tahap
│   └── CBR.ipynb
└── README.md           # File ini
```

## 🚀 Cara Instalasi

### 1. Clone repository:
```bash
git clone https://github.com/NadiaHumairaa/UAS-PENALARAN_KOMPUTER-233.git
cd nama-repo
```

### 2. Buat virtual environment (opsional tapi direkomendasikan):
```bash
python -m venv venv
source venv/bin/activate      # Linux/macOS
venv\Scripts\activate       # Windows
```

## ▶️ Menjalankan Pipeline (End-to-End)

Notebook utama adalah:  
📄 `notebooks/CBR.ipynb`

### Langkah-langkah:
1. Jalankan setiap cell dari awal sampai akhir
2. Notebook mencakup:
   - Preprocessing teks putusan (cleaning, stemming, stopword removal)
   - TF-IDF vectorization
   - Klasifikasi berdasarkan similaritas cosine (CBR)
   - Evaluasi hasil prediksi

## 📊 Hasil Evaluasi

Model CBR diuji menggunakan pembagian data training dan testing dari dataset lokal.  
Evaluasi menggunakan metrik:
- Accuracy
- Precision
- Recall
- F1-Score

📈 Hasil evaluasi dan visualisasi terdapat pada bagian akhir notebook.

## 🧠 Metodologi

Metode yang digunakan adalah **Case-Based Reasoning (CBR)** 5 tahap:
1. **Retrieve**: Mengambil kasus serupa menggunakan Cosine Similarity
2. **Reuse**: Menggunakan hasil dari kasus serupa untuk memprediksi label
3. **Revise**: Validasi hasil prediksi terhadap ground truth
4. **Retain**: Menambahkan kasus baru ke basis kasus jika relevan
5. **Explanation**: Menjelaskan hasil sistem berbasis similarity

## 🔧 Library yang Digunakan

- `pandas`
- `numpy`
- `sklearn`
- `nltk`
- `Sastrawi`
- `matplotlib`

## 📌 Sumber Data

Dataset diperoleh dari:
> Direktori Putusan Mahkamah Agung RI  
> Kategori: **Pidana Khusus > Narkotika dan Psikotropika**  
> Lokasi: **Pengadilan Negeri Kandangan**  
> [https://putusan3.mahkamahagung.go.id](https://putusan3.mahkamahagung.go.id)

## 👨‍🎓 Disusun Oleh:

- **Nama**: [Nadia Humaira]
- **NIM**: [202110370311233]
- **Kelas**: [Penalaran Komputer (C)]

## 📄 Lisensi

Repositori ini digunakan untuk keperluan akademik.  
Lisensi mengikuti hak cipta dari Mahkamah Agung RI terkait data.
