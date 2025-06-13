# Real-Time Sentiment Analysis for Bank BCA Products

Proyek ini membangun sistem analisis sentimen berbasis machine learning dari awal (tanpa model pre-trained) untuk mengevaluasi persepsi publik terhadap produk-produk dari Bank BCA. Sistem dilengkapi antarmuka berbasis Streamlit untuk inferensi manual dan batch.

## Fitur Utama

- Scraping review dari berbagai sumber (Google Play, forum simulasi, YouTube, dsb)
- Preprocessing teks dan pelatihan model TensorFlow (dari awal, bukan pre-trained)
- Prediksi sentimen real-time dengan antarmuka Streamlit
- Dukungan input manual dan upload file CSV

## Struktur Proyek

```
.
├── ml_app/
│   ├── model/
│       ├── sentiment_model.h5
│       └── tokenizer.pkl
├── requirements.txt
└── README.md
```

## Cara Menjalankan (Lokal)

### 1. Install dependensi

```bash
pip install -r requirements.txt
```

### 2. Jalankan Streamlit app

```bash
streamlit run interface/streamlit_app_bca.py
```

### 3. Upload CSV (opsional)

Format:

```csv
review
Saya suka fitur BCA mobile
Sangat lambat dan sering error
```

## Model

- Dibangun menggunakan TensorFlow LSTM dari nol
- Tokenisasi menggunakan `Tokenizer` + `pad_sequences`
- Label: biner (positif / negatif)

## Sumber Data

- Sentiment140 (Dataset pelatihan awal)
- Scraped review: Google Play, forum simulasi, YouTube, TikTok, Google Maps (rencana)

## Catatan

- Model dan UI ini dikembangkan untuk keperluan edukatif & eksperimental
- Data yang digunakan hanya data publik
- Tidak menggunakan model pre-trained dari TensorFlow Hub, HuggingFace, dll.

## Kontributor

- Bainul Dwi Tri Putra

## 📃 Lisensi

MIT License

