# 🍄 Rama_09020282529067_TakeHomeML

> **Take Home Machine Learning — Mushroom Classification**

Repository ini berisi pengerjaan **Take Home Machine Learning** dengan studi kasus **Mushroom Classification**.

Project ini bertujuan untuk menganalisis dataset mushroom, melakukan **Exploratory Data Analysis (EDA)**, melakukan preprocessing data, membangun model **Machine Learning klasik**, melakukan eksperimen **Deep Learning**, melakukan evaluasi model, serta menganalisis hasil prediksi.

---

## 👤 Identitas

| Informasi | Detail |
|---|---|
| **Nama** | Rama |
| **NIM** | 09020282529067 |
| **Project** | Take Home Machine Learning |
| **Repository** | `Rama_09020282529067_TakeHomeML` |
| **Topik** | Mushroom Classification |
| **Problem Type** | Binary Classification |
| **Bahasa Pemrograman** | Python |

---

# 🎯 Problem Statement

Pertanyaan utama dalam project ini adalah:

> **Can Machine Learning Identify Whether a Mushroom is Edible or Poisonous?**

Permasalahan tersebut merupakan **Binary Classification Problem** karena target yang diprediksi memiliki dua kelas:

| Label | Keterangan |
|---|---|
| `e` | Edible |
| `p` | Poisonous |

Tujuan utama project adalah mengetahui apakah karakteristik mushroom pada dataset dapat digunakan oleh Machine Learning untuk membedakan mushroom **Edible** dan **Poisonous**.

---

# 📊 Dataset

Dataset yang digunakan adalah **Mushroom Dataset**.

Dataset berisi berbagai karakteristik mushroom yang sebagian besar berupa fitur kategorikal.

Target yang digunakan dalam proses klasifikasi adalah:

```text
class
```

Dengan kategori:

```text
e = Edible
p = Poisonous
```

### Distribusi Target

Berdasarkan hasil eksplorasi dataset:

| Class | Jumlah |
|---|---:|
| Edible (`e`) | 4.208 |
| Poisonous (`p`) | 3.916 |
| **Total** | **8.124** |

Distribusi kedua kelas relatif seimbang dengan selisih sebanyak **292 data**.

Kondisi tersebut cukup baik untuk proses klasifikasi karena tidak terdapat ketidakseimbangan kelas yang ekstrem.

---

# 🔎 Exploratory Data Analysis

Exploratory Data Analysis atau **EDA** dilakukan untuk memahami karakteristik dataset sebelum masuk ke tahap Machine Learning.

Tahapan EDA meliputi:

1. Memahami struktur dataset
2. Memeriksa jumlah data
3. Memeriksa tipe data
4. Memeriksa missing value
5. Memeriksa duplicate
6. Menganalisis distribusi target
7. Menganalisis distribusi fitur
8. Menganalisis hubungan fitur dengan target
9. Mengidentifikasi fitur yang berpotensi penting

---

## 📌 Target Distribution

Hasil distribusi target menunjukkan:

- **4.208** data Edible
- **3.916** data Poisonous

Distribusi tersebut menunjukkan bahwa dataset relatif balanced.

Dengan distribusi yang cukup seimbang, model tidak terlalu didominasi oleh salah satu kelas.

---

# 📈 Feature Distribution

Beberapa fitur yang dianalisis dalam proses EDA antara lain:

- `odor`
- `bruises`
- `gill-size`
- `cap-color`
- `habitat`

Analisis distribusi dilakukan untuk mengetahui kategori yang paling banyak muncul pada setiap fitur.

Hasil analisis menunjukkan bahwa beberapa kategori memiliki jumlah data yang jauh lebih banyak dibandingkan kategori lainnya.

Hal ini menunjukkan bahwa distribusi beberapa fitur tidak sepenuhnya merata pada seluruh kategori.

---

# 🔗 Feature vs Target

Analisis berikutnya dilakukan dengan melihat hubungan antara fitur dengan target `class`.

### `odor`

Fitur `odor` menunjukkan hubungan yang sangat jelas dengan target.

Beberapa kategori `odor` hampir sepenuhnya didominasi oleh salah satu kelas, yaitu Edible atau Poisonous.

Hal tersebut menunjukkan bahwa `odor` merupakan salah satu fitur yang sangat informatif dalam proses klasifikasi.

### `gill-size`

Fitur `gill-size` juga menunjukkan perbedaan proporsi yang cukup jelas antara kedua kelas.

Kategori tertentu lebih banyak ditemukan pada Edible, sedangkan kategori lainnya lebih banyak ditemukan pada Poisonous.

### `bruises`

Fitur `bruises` menunjukkan pola distribusi yang berbeda antara kelas Edible dan Poisonous.

Perbedaan proporsi tersebut menunjukkan bahwa fitur ini memiliki informasi yang dapat membantu proses klasifikasi.

### `habitat`

Fitur `habitat` menunjukkan bahwa beberapa kategori lebih dominan pada Edible, sedangkan kategori lainnya lebih dominan pada Poisonous.

---

# 💡 Insight Utama EDA

Berdasarkan hasil EDA, beberapa insight utama yang diperoleh adalah:

1. Dataset memiliki dua kelas utama, yaitu Edible dan Poisonous.
2. Distribusi target relatif seimbang.
3. Fitur `odor` menunjukkan hubungan yang sangat kuat dengan target.
4. Fitur `gill-size` menunjukkan perbedaan proporsi yang cukup jelas antara kedua kelas.
5. Fitur `bruises` juga menunjukkan pola yang berbeda antara Edible dan Poisonous.
6. Fitur `habitat` memiliki distribusi kelas yang berbeda pada beberapa kategorinya.
7. Beberapa fitur memiliki kategori yang jumlah datanya tidak merata.

---

# 🧹 Data Preprocessing

Sebelum digunakan untuk membangun model, dataset melalui beberapa tahapan preprocessing.

Tahapan preprocessing meliputi:

```text
Raw Dataset
     ↓
Data Inspection
     ↓
Missing Value Check
     ↓
Duplicate Check
     ↓
Feature & Target Separation
     ↓
Categorical Encoding
     ↓
Train-Test Split
     ↓
Model Training
```

Karena sebagian besar fitur merupakan data kategorikal, dilakukan proses encoding agar data dapat digunakan oleh algoritma Machine Learning.

---

# 🤖 Machine Learning Models

Beberapa algoritma Machine Learning klasik digunakan dalam project ini.

## 1. Logistic Regression

Logistic Regression digunakan sebagai **baseline model**.

Model ini digunakan untuk mengetahui performa pendekatan klasifikasi yang relatif sederhana terhadap dataset.

---

## 2. Decision Tree

Decision Tree digunakan untuk mempelajari pola data melalui struktur percabangan.

Model dapat membuat keputusan berdasarkan kondisi tertentu pada fitur.

---

## 3. Random Forest

Random Forest merupakan algoritma ensemble yang terdiri dari beberapa Decision Tree.

Random Forest digunakan karena mampu menangkap hubungan yang lebih kompleks dan biasanya memiliki kemampuan generalisasi yang lebih baik dibandingkan satu Decision Tree.

---

# 📏 Model Evaluation

Evaluasi model dilakukan menggunakan beberapa metrik:

- Accuracy
- Precision
- Recall
- F1-Score
- Confusion Matrix

### Accuracy

Mengukur persentase prediksi yang benar dari seluruh data.

### Precision

Mengukur ketepatan prediksi positif yang dilakukan oleh model.

### Recall

Mengukur kemampuan model dalam menemukan data dari suatu kelas.

### F1-Score

Merupakan kombinasi antara Precision dan Recall.

### Confusion Matrix

Digunakan untuk melihat:

- True Positive
- True Negative
- False Positive
- False Negative

Penggunaan beberapa metrik diperlukan agar evaluasi model tidak hanya bergantung pada Accuracy.

---

# 🧠 Deep Learning

Selain Machine Learning klasik, dilakukan eksperimen menggunakan **Deep Learning dengan TensorFlow/Keras**.

Secara umum arsitektur Neural Network terdiri dari:

```text
Input Layer
     ↓
Hidden Layer
     ↓
Hidden Layer
     ↓
Output Layer
```

Model Deep Learning digunakan sebagai pembanding terhadap Machine Learning klasik.

Evaluasi dilakukan menggunakan:

- Training Accuracy
- Validation Accuracy
- Test Accuracy
- Training Loss
- Validation Loss

---

# ⚙️ Hyperparameter Tuning

Hyperparameter tuning dilakukan untuk mencari konfigurasi model yang lebih optimal.

Parameter yang dapat digunakan pada Random Forest antara lain:

```text
n_estimators
max_depth
min_samples_split
min_samples_leaf
```

Tujuan tuning adalah meningkatkan performa model sekaligus mempertahankan kemampuan generalisasi terhadap data baru.

---

# 🔍 Feature Importance

Feature Importance digunakan untuk mengetahui fitur yang paling berkontribusi terhadap prediksi model.

Hasil feature importance kemudian dibandingkan dengan hasil EDA.

Fitur yang menjadi perhatian utama adalah:

```text
odor
gill-size
bruises
```

Hal ini karena fitur-fitur tersebut sebelumnya menunjukkan pola yang cukup kuat terhadap target `class`.

---

# 📉 Overfitting Analysis

Overfitting dianalisis dengan membandingkan performa model pada data training dan testing.

Konsep dasarnya:

```text
Training Performance
        vs
Testing Performance
```

Jika performa training jauh lebih tinggi dibandingkan testing, maka terdapat indikasi overfitting.

Sebaliknya, apabila performa training dan testing relatif berdekatan, model memiliki kemampuan generalisasi yang lebih baik.

Analisis ini penting untuk memastikan model tidak hanya mempelajari atau menghafal data training, tetapi juga mampu melakukan prediksi terhadap data yang belum pernah dilihat sebelumnya.

---

# ❌ Error Analysis

Error Analysis dilakukan untuk memahami kesalahan prediksi model.

Terdapat dua jenis kesalahan yang menjadi perhatian utama:

### False Positive

Mushroom sebenarnya **Edible**, tetapi diprediksi sebagai **Poisonous**.

### False Negative

Mushroom sebenarnya **Poisonous**, tetapi diprediksi sebagai **Edible**.

Dalam konteks klasifikasi mushroom, **False Negative perlu mendapat perhatian khusus** karena mushroom yang sebenarnya Poisonous tetapi diprediksi sebagai Edible dapat memiliki konsekuensi yang lebih serius.

Oleh karena itu, Recall dan Confusion Matrix menjadi metrik yang penting untuk diperhatikan.

---

# 🔬 Regression Exploration

Regression Exploration dilakukan sebagai eksperimen tambahan untuk memahami perbedaan antara **Classification** dan **Regression**.

Dataset Mushroom merupakan permasalahan **Classification**, bukan Regression.

Hal tersebut dikarenakan target yang ingin diprediksi berupa kategori:

```text
e = Edible
p = Poisonous
```

Bukan nilai numerik kontinu.

Sehingga pendekatan yang tepat untuk permasalahan utama adalah:

```text
Mushroom Dataset
       ↓
Binary Classification
       ↓
Edible / Poisonous
```

Regression Exploration digunakan sebagai pembelajaran tambahan mengenai perbedaan antara regression dan classification.

---

# 📋 Project Workflow

Keseluruhan proses project dilakukan dengan alur:

```text
Mushroom Dataset
       ↓
Data Understanding
       ↓
Exploratory Data Analysis
       ↓
Data Preprocessing
       ↓
Train-Test Split
       ↓
┌───────────────────────────────┐
│       Machine Learning        │
│                               │
│  Logistic Regression          │
│  Decision Tree                │
│  Random Forest                │
└───────────────────────────────┘
       ↓
Model Evaluation
       ↓
Hyperparameter Tuning
       ↓
Feature Importance
       ↓
Deep Learning
       ↓
Overfitting Analysis
       ↓
Error Analysis
       ↓
Regression Exploration
       ↓
Conclusion
```

---

# 🗂️ Project Structure

```text
Rama_09020282529067_TakeHomeML/
│
├── dataset/
│   └── mushrooms.csv
│
├── notebook/
│   └── Rama_09020282529067_TakeHomeML.ipynb
│
├── README.md
├── requirements.txt
└── .gitignore
```

### Penjelasan Struktur

| File / Folder | Keterangan |
|---|---|
| `dataset/` | Menyimpan dataset |
| `mushrooms.csv` | Dataset mushroom |
| `notebook/` | Menyimpan Jupyter Notebook |
| `README.md` | Dokumentasi project |
| `requirements.txt` | Daftar library Python |
| `.gitignore` | File yang tidak perlu di-upload ke Git |

---

# 🛠️ Technologies & Libraries

Project ini menggunakan:

| Technology / Library | Penggunaan |
|---|---|
| Python | Bahasa pemrograman |
| Pandas | Data manipulation dan analysis |
| NumPy | Numerical computation |
| Matplotlib | Data visualization |
| Seaborn | Statistical visualization |
| Scikit-learn | Machine Learning |
| TensorFlow | Deep Learning |
| Keras | Neural Network |
| Jupyter Notebook | Eksperimen dan dokumentasi |

---

# 🚀 Installation

## 1. Clone Repository

```bash
git clone <URL_REPOSITORY>
```

Masuk ke folder project:

```bash
cd Rama_09020282529067_TakeHomeML
```

---

## 2. Membuat Virtual Environment

Disarankan menggunakan virtual environment agar dependency project terisolasi.

```bash
python -m venv .venv
```

### Linux / macOS

```bash
source .venv/bin/activate
```

### Windows

```powershell
.venv\Scripts\activate
```

---

## 3. Install Dependencies

Install library yang dibutuhkan:

```bash
pip install -r requirements.txt
```

---

# ▶️ Running Notebook

Jalankan Jupyter Notebook:

```bash
jupyter notebook
```

atau:

```bash
jupyter lab
```

Kemudian buka:

```text
notebook/Rama_09020282529067_TakeHomeML.ipynb
```

Jalankan notebook secara berurutan mulai dari cell pertama hingga bagian conclusion.

---

# 📦 Requirements

Library utama yang digunakan:

```text
numpy
pandas
matplotlib
seaborn
scikit-learn
tensorflow
jupyter
ipykernel
```

Install seluruh dependency dengan:

```bash
pip install -r requirements.txt
```

---

# 🧪 Reproducibility

Beberapa proses Machine Learning menggunakan `random_state` untuk membantu menghasilkan eksperimen yang konsisten.

Contoh:

```python
from sklearn.model_selection import train_test_split

X_train, X_test, y_train, y_test = train_test_split(
    X,
    y,
    test_size=0.2,
    random_state=42,
    stratify=y
)
```

Penggunaan `stratify=y` membantu mempertahankan proporsi kelas Edible dan Poisonous pada data training dan testing.

---

# 🏆 Model Performance

Performa model dibandingkan menggunakan beberapa metrik evaluasi.

| Model | Accuracy | Precision | Recall | F1-Score |
|---|---:|---:|---:|---:|
| Logistic Regression | - | - | - | - |
| Decision Tree | - | - | - | - |
| Random Forest | - | - | - | - |
| Deep Learning | - | - | - | - |

> **Note:** Nilai performa diisi berdasarkan hasil eksperimen pada notebook.

Model terbaik ditentukan berdasarkan keseluruhan metrik evaluasi dan kemampuan generalisasi, bukan hanya berdasarkan Accuracy.

---

# 🎓 Conclusion

Berdasarkan seluruh proses yang dilakukan, dataset Mushroom merupakan dataset yang sesuai untuk permasalahan **Binary Classification** karena target yang ingin diprediksi terdiri dari dua kelas, yaitu Edible dan Poisonous.

Hasil Exploratory Data Analysis menunjukkan bahwa beberapa fitur memiliki pola yang cukup kuat terhadap target, terutama `odor`, `gill-size`, dan `bruises`. Fitur `odor` menunjukkan hubungan yang paling jelas karena beberapa kategorinya sangat didominasi oleh salah satu kelas.

Machine Learning klasik yang digunakan dalam project ini meliputi Logistic Regression, Decision Tree, dan Random Forest. Selain itu, dilakukan eksperimen menggunakan Deep Learning sebagai pembanding.

Evaluasi dilakukan menggunakan Accuracy, Precision, Recall, F1-Score, dan Confusion Matrix. Analisis training dan testing juga dilakukan untuk mengetahui kemungkinan terjadinya overfitting.

Hasil akhir dari project ini digunakan untuk memahami bagaimana Machine Learning dapat mempelajari pola karakteristik mushroom dan menggunakannya untuk membedakan kelas Edible dan Poisonous.

Namun, model yang dibuat merupakan bagian dari **eksperimen dan pembelajaran Machine Learning** dan tidak boleh digunakan sebagai satu-satunya dasar untuk menentukan keamanan mushroom nyata untuk dikonsumsi.

---

# ❓ Answer to the Main Question

> **Can Machine Learning Identify Whether a Mushroom is Edible or Poisonous?**

**Yes.**

Machine Learning dapat mempelajari pola dari karakteristik mushroom pada dataset dan menggunakannya untuk melakukan klasifikasi antara **Edible** dan **Poisonous**.

Namun, tingkat keberhasilan model tetap bergantung pada:

- kualitas dataset,
- preprocessing,
- pemilihan fitur,
- algoritma,
- hyperparameter,
- dan kemampuan generalisasi model.

Prediksi Machine Learning tetap memiliki kemungkinan mengalami kesalahan sehingga tidak dapat dianggap sebagai pengganti identifikasi mushroom oleh ahli.

---

# ⚠️ Disclaimer

Project ini dibuat untuk:

- Pembelajaran Machine Learning
- Exploratory Data Analysis
- Eksperimen klasifikasi
- Perbandingan algoritma
- Eksperimen Deep Learning
- Analisis model

Model yang dibuat **tidak dimaksudkan sebagai alat keamanan pangan atau alat untuk menentukan apakah mushroom nyata aman dikonsumsi**.

---

# 🎓 Learning Outcomes

Melalui project ini, beberapa konsep yang dipelajari meliputi:

- Data Understanding
- Exploratory Data Analysis
- Data Cleaning
- Data Preprocessing
- Categorical Encoding
- Train-Test Split
- Binary Classification
- Logistic Regression
- Decision Tree
- Random Forest
- Hyperparameter Tuning
- Model Evaluation
- Confusion Matrix
- Feature Importance
- Deep Learning
- Overfitting Analysis
- Error Analysis
- Classification vs Regression

---

# 👨‍💻 Author

**Rama**

**NIM:** `09020282529067`

**Project:** `Rama_09020282529067_TakeHomeML`

---

<p align="center">
  <b>🍄 Mushroom Classification — Take Home Machine Learning</b>
</p>