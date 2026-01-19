#  Sentiment Analysis on Social Media Data (Classical ML)

##  Overview
Proyek ini bertujuan untuk melakukan analisis sentimen pada data media sosial (**SocialBuzz**) menggunakan pendekatan Machine Learning klasik. Fokus utama proyek ini adalah membandingkan performa model probabilistik (**Naive Bayes**) dengan model berbasis *hyperplane* (**Support Vector Machine / SVM**) serta melakukan optimalisasi *preprocessing* teks untuk menangani data yang tidak seimbang (*imbalanced*).

##  Tech Stack
* **Python 3.10+**
* **Scikit-Learn** (Modeling & Pipeline)
* **Pandas & NumPy** (Data Manipulation)
* **NLTK** (Text Preprocessing: Lemmatization, Stopwords)
* **Matplotlib & Seaborn** (Visualization)

##  Key Features
1.  **Text Preprocessing Pipeline:**
    * Cleaning (Regex, Lowercasing).
    * **Advanced Lemmatization** (menangani kata dasar lebih baik daripada Stemming).
    * Handling Negation (memastikan kata seperti "not good" tidak kehilangan makna).
2.  **Feature Engineering:**
    * **TF-IDF Vectorization** dengan Unigram & Bigram.
    * **Character N-Grams** untuk menangani *typo* dan bahasa gaul.
3.  **Model Optimization:**
    * Hyperparameter Tuning menggunakan **GridSearchCV**.
    * **Cost-Sensitive Learning** pada SVM untuk menangani *Class Imbalance*.

## 📈 Results & Benchmarks
Berdasarkan eksperimen pada data uji (*Test Set*):

| Model | Accuracy | F1-Score (Macro) | Keterangan |
| :--- | :--- | :--- | :--- |
| **Naive Bayes** | ~74% | 0.70 | Cepat, namun kurang peka terhadap konteks. |
| **Logistic Regression**| ~75% | 0.72 | Baseline yang solid, sedikit overfitting. |
| **SVM (Linear)** | **~78%** | **0.76** | **Best Performer** setelah tuning regulerisasi (C). |

**Insight:** SVM bekerja lebih baik pada data teks berdimensi tinggi dibandingkan Naive Bayes karena kemampuannya menemukan *decision boundary* yang optimal antar kelas sentimen.
3.  Jalankan notebook: `Classical_Sentiment_Analysis.ipynb`

---
