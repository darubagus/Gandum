# Descriptive Statistics and Hypothesis Testing

Program ini dibuat untuk memenuhi tugas Mata Kuliah **IF2220 Probabilitas dan Statistika** <br />

*Program Studi Teknik Informatika* <br />
*Sekolah Teknik Elektro dan Informatika* <br />
*Institut Teknologi Bandung* <br />

*Semester II Tahun 2020/2021*

---
## Description

---
### **Tes Distribusi Normal**

#### **D'Agostino-Pearson Normality Test**

D'Agostino-Pearson Normality Test dilakukan dengan mengkombinasikan Skewness test dan Kurtosis test yang dalam program ini dilakukan dengan memanggil fungsi ```stats.normaltest({dataframe})``` dari library *scipy* kemudian divisualisasikan dengan ```sns.distplot({dataframe})``` dari library *seaborn*. <br>
<br>
Pada test ini, digunakan persamaan : <br><br>

$K^2 = Z_s^2 + Z_k^2$. $Z_s$ <br><br>

dengan $Z_s$ merupakan hasil skewness test, $Z_k$ merupakan hasil kurtosis test. $K^2$ diperoleh dengan cara aproksimasi terdistribusi dengan menggunakan $\chi^2$ (chi-squared) dengan derajat kebebasan $2$<br><br>

Hipotesis null ($H_0$) default dari test ini adalah masing-masing kolom yang dites terdistribusi normal. Normality test dengan menggunakan metode ini akan menghasilkan dua nilai, yaitu stat dan $p$. Apabila $p > \alpha$, maka $H_0$ diterima sehingga dapat disimpulkan bahwa kolom terdistribusi normal. Sedangkan jika $p < \alpha $, maka $H_0$ ditolak sehingga disimpulkan bahwa kolom tidak terdistribusi normal.

---
### **Tes Hipotesis dengan 1 Sampel**

***Langkah Testing***
1. Tentukan Hipotesis nol ($H_0$: θ = $θ_0$), dimana θ bisa berupa μ, σ2, p, atau data lain berdistribusi tertentu (normal, binomial, dsc.).
2. Pilih hipotesis alternatif $H_1$ salah dari dari θ > $θ_0$, θ < $θ_0$, atau θ ≠ $θ_0$.
3. Tentukan tingkat signifikan α.
4. Tentukan uji statistik yang sesuai dan tentukan daerah kritis.
5. Hitung nilai uji statistik dari data sample. Hitung p-value sesuai dengan uji statistik yang digunakan.
6. Ambil keputusan dengan TOLAK $H_0$ jika nilai uji terletak di daerah kritis atau dengan tessignifikan, TOLAK $H_0$ jika p-value lebih kecil dibanding tingkat signifikansi α yang diinginkan

---
### **Tes Hipotesis dengan 2 Sampel**

***Langkah Testing***
1. Tentukan Hipotesis nol ($H_0$: θ = $θ_0$), dimana θ bisa berupa μ, σ2, p, atau data lain berdistribusi tertentu (normal, binomial, dsc.).
2. Pilih hipotesis alternatif $H_1$ salah dari dari θ > $θ_0$, θ < $θ_0$, atau θ ≠ $θ_0$.
3. Tentukan tingkat signifikan α.
4. Tentukan uji statistik yang sesuai dan tentukan daerah kritis.
5. Hitung nilai uji statistik dari data sample. Hitung p-value sesuai dengan uji statistik yang digunakan.
6. Ambil keputusan dengan TOLAK $H_0$ jika nilai uji terletak di daerah kritis atau dengan tessignifikan, TOLAK $H_0$ jika p-value lebih kecil dibanding tingkat signifikansi α yang diinginkan

---
### **Tes Korelasi**
Test korelasi menggunakan metode Pearson Product Moment Correlation akan menghasilkan Pearson correlation coefficient pada rentang $(-1 ≤ r ≤ 1)$ untuk suatu random variable $X$ dan $Y$

*   r = 1, maka kedua kolom yang dibandingkan memiliki korelasi positif sempurna, artinya jika nilai $X$ membesar, maka nilai $Y$ juga membesar dan *vice versa*
*   Bila $r > 0$, maka kolom $X$ dan $Y$ memiliki korelasi positif
* Bila $r = 0$, maka kolom $X$ dan $Y$ tidak memiliki korelasi
* Bila $r < 0$, maka kolom $X$ dan $Y$ memiliki korelasi negatif
* Bila $r = -1$, maka maka kedua kolom yang dibandingkan memiliki korelasi negatif sempurna, artinya jika nilai $X$ membesar, maka nilai $Y$ mengecil dan *vice versa*.
<br>
<br>

**Klasifikasi Pearson correlation coefficient** <br>
* Perfect Correlation $\rightarrow r = \pm 1$
* High Degree Correlation $\rightarrow 0.5 ≤ r ≤ 1$ or $-1 ≤ r ≤ -0.5$
* Moderate Degree Correlation $\rightarrow 0.3 ≤ r ≤ 0.49$ or $-0.49 ≤ r ≤ -0.3$
* Low Degree Correlation $\rightarrow  0 < r ≤ 0.29$ or $-0.29 ≤ r < 0$
* No Correlation $\rightarrow  r = 0$
