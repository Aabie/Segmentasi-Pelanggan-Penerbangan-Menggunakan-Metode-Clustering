# Airline Customer Value Analysis Case with Clustering KMeans
Project ini bertujuan untuk melakukan analisis nilai pelanggan pada sebuah maskapai penerbangan menggunakan algoritma clustering KMeans. Dalam proyek ini, data pelanggan maskapai penerbangan akan dianalisis berdasarkan fitur-fitur tertentu seperti jumlah penerbangan yang dilakukan, nilai transaksi, dan lain-lain.

# DATA
Data yang digunakan dalam project ini adalah dataset maskapai penerbangan yang diperoleh dari sumber terbuka. Dataset ini berisi informasi tentang pelanggan, termasuk fitur-fitur seperti Recency, Frequency, dan Monetary. Data tersebut terdapat dalam file flight.csv

# Reqruirments
- Python 3.x
- Libraries:
    1. Pandas
    2. Scikit-learn
    3. Seaborn
    4. Matplotlib
    5. Numpy

# Content

## EDA
Berdasarkan informasi yang didapatkan dari dataset didapatkan bahwa :
1. Mayoritas customer adalah `Pria (76.4%)`
2. Sebanyak 91.7% customer berasal dari negara `CN`
3. Mayoritas data numerical bersifat `positive Skewed` dan dapat diasumsikan memiliki `outlier`
4. Banyak data yang bersifat memiliki korelasi tinggi (> 0.7)

## Preprocessing
1. Type data 
2. Feature Selection (menggunakan RFM)
    - Recency : LAST_TO_END (Jarak waktu penerbangan terakhir ke pesanan penerbangan paling akhir)
    - Frequency : FLIGHT_COUNT (Jumlah penerbangan Customer)
    - Monetary : avg_discount (Rata rata discount yang didapat customer)
3. Missing Value & Duplicate
4. Outlier Treatment
5. Standardization

## Modeling
Model yang dipakai dalam project ini adalah KMeans yang dinilai memiliki efisiensi dalam pemrosesan data, mudah diimplementasikan, menghasilkan hasil clustering yang stabil dan konsisten, serta cocok untuk data numerik. KMeans mampu memproses data yang besar dengan cepat karena algoritma ini memiliki kompleksitas waktu yang cukup rendah.Project ini menggunakan data yang dilakukan dimensional reduction untuk memudahkan visualisasi dari hasil clustering customer. 

# Hasil & Pembahasan
dari hasil modeling yang dilakukan didapatkan 4 hasil cluster yaitu :
- Cluster 0 : Customer yang memiliki jarak waktu penerbangan terakhir sekitar 53 hari, dengan frekuensi penerbangan sekitar 21 kali penerbangan, dan rata rata discount sekitar 0.72%
- Cluster 1 : Customer yang memiliki jarak waktu penerbangan terakhir sekitar 118 hari, dengan frekuensi penerbangan sekitar 7 kali penerbangan, dan rata rata discount sekitar 0.56%
- Cluster 2 : Customer yang memiliki jarak waktu penerbangan terakhir sekitar 115 hari, dengan frekuensi penerbangan sekitar 7 kali penerbangan, dan rata rata discount sekitar 0.81%
- Cluster 3 : Customer yang memiliki jarak waktu penerbangan terakhir sekitar 435 hari, dengan frekuensi penerbangan sekitar 4 kali penerbangan, dan rata rata discount sekitar 0.71%

# Kontributor
- Abie Nugraha