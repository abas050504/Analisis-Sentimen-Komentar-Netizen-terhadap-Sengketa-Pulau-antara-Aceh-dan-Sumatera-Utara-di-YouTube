## 📘 Pendahuluan

Sengketa empat pulau antara Provinsi Aceh dan Sumatera Utara—yaitu Pulau Mangkir Ketek, Pulau Mangkir Gadang, Pulau Lipan, dan Pulau Panjang—telah memicu perdebatan yang luas di masyarakat, terutama di media sosial seperti YouTube. Banyak komentar publik menunjukkan ketidakpuasan terhadap keputusan pemerintah terkait batas wilayah, seperti desakan pencopotan pejabat hingga dukungan terhadap integritas Aceh dalam NKRI.

Melalui proyek ini, dilakukan analisis sentimen terhadap 2.602 komentar YouTube untuk memahami opini publik terhadap isu ini. Proyek ini menggunakan pendekatan Natural Language Processing (NLP) dan algoritma machine learning untuk klasifikasi sentimen.

---

## 🔍 Metodologi Penelitian

Penelitian ini dilakukan dengan beberapa tahapan utama sebagai berikut:

1. **Pengumpulan Data**
   - Menggunakan teknik scraping untuk mengambil 2.602 komentar dari video YouTube terkait sengketa pulau Aceh-Sumut.

2. **Preprocessing Teks**
   - Case folding (mengubah semua teks ke huruf kecil)
   - Cleaning simbol, angka, dan URL
   - Stopword removal
   - Stemming menggunakan Sastrawi

3. **Labeling Komentar**
   - Pelabelan otomatis berbasis keyword:
     - Contoh: "wilayah Aceh" → pro_aceh, "wilayah Sumut" → pro_sumut

4. **Ekstraksi Fitur**
   - Menggunakan metode TF-IDF untuk mengubah data teks menjadi bentuk numerik.

5. **Modeling**
   - Menggunakan tiga algoritma klasifikasi:
     - Naïve Bayes
     - Logistic Regression
     - Random Forest

6. **Evaluasi Model**
   - Menggunakan metrik:
     - Akurasi
     - Precision
     - Recall
     - F1-score

---

## 📊 Hasil dan Evaluasi

Distribusi data komentar berdasarkan label:

- **Pro Aceh:** 943 komentar
- **Pro Sumut:** 17 komentar
- **Tidak Jelas:** 1.642 komentar

### 🔢 Evaluasi Model

| Algoritma           | Akurasi  | F1-score |
|---------------------|----------|----------|
| Random Forest       | 92.13%   | 74.09%   |
| Logistic Regression | 89.25%   | 58.42%   |
| Naïve Bayes         | 86.18%   | 55.77%   |

- Model Random Forest memberikan performa terbaik untuk klasifikasi sentimen komentar yang tidak seimbang.

- Beberapa **kata kunci penting** yang dominan dalam komentar:
  - `"aceh"`, `"pecat"`, `"dukung"`, `"tito"`, `"copot"`

---

## ✅ Kesimpulan

- Mayoritas komentar netizen di YouTube bersifat **netral** atau **mendukung Aceh**.
- Jumlah komentar **pro Sumut** sangat sedikit, yang memengaruhi performa model dalam mengenali kelas tersebut.
- Algoritma **Random Forest** terbukti paling efektif untuk klasifikasi komentar pada isu ini.
- WordCloud dan fitur penting dalam model mengonfirmasi bahwa opini publik didominasi oleh narasi dukungan terhadap Aceh dan penolakan terhadap keputusan pusat.

---

## 📎 Referensi Utama

> Monika, T., Aura, V., Basri, M.H., Purnawan, I., & Suhaidi, A. (2024). *Analisis Sentimen Komentar Pengguna Media Sosial terhadap Sengketa Empat Pulau antara Aceh dan Sumatera Utara*. Jurnal Teknologi Informasi, Universitas Teuku Umar.
