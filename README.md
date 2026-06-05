# UTS - Klasifikasi Teks: Deteksi Ujaran Kebencian (Hate Speech) pada Tweet Berbahasa Indonesia

[![Python](https://img.shields.io/badge/Python-3.10+-blue.svg)](https://www.python.org/)
[![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-orange.svg)](https://jupyter.org/)
[![License](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)

Proyek ini merupakan **Ujian Tengah Semester (UTS)** untuk mata kuliah **Analisis Teks**.

## 🎯 Tujuan Proyek

Membangun model **klasifikasi teks** (supervised learning) untuk mendeteksi secara otomatis apakah sebuah tweet berbahasa Indonesia mengandung **ujaran kebencian (Hate Speech)** atau tidak.

Proyek ini terinspirasi dari isu terkini penyebaran hoax dan hate speech di media sosial Indonesia yang mengancam kerukunan sosial dan kesehatan mental masyarakat.

## 📄 Artikel yang Diangkat

**Judul:** Analisis Penyebaran Informasi Palsu dan Ujaran Kebencian di Media Sosial Indonesia : Studi Kasus Berita Hoax dan Hate Speech  
**Penulis:** S. Ramadhani (2025)  
**Jurnal:** Publistik: Jurnal Ilmu Komunikasi  
**Link:** [Baca Artikel](https://ejurnal.iainpare.ac.id/index.php/publistikji/article/view/14654/2959)  
**PDF:** [Download Full Artikel](https://ejurnal.iainpare.ac.id/index.php/publistikji/article/download/14654/2959)

## 📊 Dataset

- **Nama Dataset:** Indonesian Multi-label Hate Speech and Abusive Language Detection Twitter Dataset
- **Sumber:** [GitHub - okkyibrohim](https://github.com/okkyibrohim/id-multi-label-hate-speech-and-abusive-language-detection)
- **Jumlah Data:** 13.169 tweet berbahasa Indonesia
- **Label:** Binary classification (`HS` = 1 untuk Hate Speech, 0 untuk Non-Hate Speech)
- **Paper Pendukung:** Ibrohim, M.O. & Budi, I. (2019). Multi-label Hate Speech and Abusive Language Detection in Indonesian Twitter.

## 🛠️ Teknologi & Library yang Digunakan

- **Python 3**
- **Pandas** & **NumPy** — manipulasi data
- **Scikit-learn** — TF-IDF, model klasifikasi (Logistic Regression & Naive Bayes), evaluasi
- **NLTK** + **Sastrawi** — tokenisasi, stopwords removal, dan stemming bahasa Indonesia
- **Gensim** — Word2Vec embedding
- **Matplotlib**, **Seaborn**, **WordCloud** — visualisasi (EDA)
- **Jupyter Notebook / Google Colab**

## 📁 Struktur Repository

```
uts-text-classification-hate-speech-indonesia/
├── UTS_Text_Classification_Hate_Speech_Detection.ipynb   # Notebook utama
├── README.md
└── (opsional) data/ atau hasil visualisasi
```

## 🚀 Cara Menjalankan Notebook

### Opsi 1: Google Colab (Paling Mudah & Direkomendasikan)

1. Buka notebook di Colab
2. Jalankan cell pertama untuk instalasi library:
   ```python
   !pip install pandas scikit-learn nltk gensim matplotlib seaborn wordcloud Sastrawi
   ```
3. Klik **Runtime → Run All**


## 📈 Hasil Model (Aktual dari Running)

### Logistic Regression (Model Utama)
| Metrik          | Nilai    |
|-----------------|----------|
| **Accuracy**    | **83.18%** |
| **Precision**   | 79.37%   |
| **Recall**      | 81.29%   |
| **F1-Score**    | **80.32%** |

### Multinomial Naive Bayes (Perbandingan)
| Metrik          | Nilai    |
|-----------------|----------|
| Accuracy        | 82.92%   |
| F1-Score        | 79.17%   |

**Kesimpulan:**  
Logistic Regression dengan `class_weight='balanced'` memberikan performa terbaik dan direkomendasikan untuk deteksi hate speech pada data Twitter Indonesia.

## 📌 Fitur yang Diimplementasikan

- ✅ Text Preprocessing lengkap (lowercasing, cleaning, tokenisasi, stopword removal, stemming dengan Sastrawi)
- ✅ Feature Engineering: **TF-IDF** + **Word2Vec**
- ✅ Exploratory Data Analysis (WordCloud, distribusi panjang teks, top words)
- ✅ Train-Test Split dengan stratifikasi
- ✅ Dua model klasifikasi + evaluasi lengkap (Accuracy, Precision, Recall, F1, Confusion Matrix)
- ✅ Dokumentasi lengkap di dalam notebook (markdown cells)

## 📚 Referensi

1. Ramadhani, S. (2025). *Analisis Penyebaran Informasi Palsu dan Ujaran Kebencian di Media Sosial Indonesia : Studi Kasus Berita Hoax dan Hate Speech*. Publistik: Jurnal Ilmu Komunikasi.
2. Ibrohim, M. O., & Budi, I. (2019). Multi-label Hate Speech and Abusive Language Detection in Indonesian Twitter. *Proceedings of the Third Workshop on Abusive Language Online*.
3. Aggarwal, C. C. (2012). A Survey of Text Clustering Algorithms. *Mining Text Data*.

## 👤 Author

**Dewa Satria**  
NIM: 25917017  
Mata Kuliah: Analisis Teks  
Dosen: Dhomas Hatta Fudholi, Ph.D.  
Universitas Islam Indonesia

---

⭐ **Jika notebook ini membantu, jangan lupa kasih star di repository!** 

Untuk pertanyaan atau saran, silakan buka issue atau hubungi saya.
