# Model-supermart-grocery

### The Goal Regression Model
Memprediksi penjualan `sale_price` perusahaan berdasarkan
1. Penjualan sebelum discount `original_price`
2. laba perusahaan `profit`
3. Diskon `discount`

### Train Model Linear Regression
Alasan saya menggunakan model ini karena jika di lihat dari tabel korelasi, ketiga kolom tersebut memiliki hubungan yang kuat yang bisa di modelnya dengan garis linear
![cortrain](https://user-images.githubusercontent.com/90812378/179354197-d31ee9ca-85e8-4b27-8c2e-eb8711c5e5e6.png)

## Linear Regression
Formula Linear Regression: $y = \alpha + \beta_1x_1 + \beta_2x_2 + \dots + \beta_nx_n$

![visres](https://user-images.githubusercontent.com/90812378/179354405-b7f73e0c-f348-4b21-aa9d-50a0efdd4092.png)

Berdasarkan gambar diatas bisa kita amati bahwa test data dengan train data sama sama menggambarkan hubungan kuat dengan `sale_price`

## Evaluasi Model

### Mean Absolute Error (MAE) atau Mean Absolute Deviation (MAD)

$MAE$ is the average of the absolute values of the errors of the predictions.

$MAE = \frac{1}{n} \sum_{i=1}^{n} |y_i - \hat{y}_i|$

Dari hasil evaluasi menggunakan **Mean Absolute Error** model kita memiliki error yang lumayan kecil yaitu MAE: 44.34559181706889. Artinya dalam melakukan prediksi tidak terjadi banyak kesalahan dalam prediksinya

### Root Mean Squared Error (RMSE)
$RMSE$ is the rooted average of the squares of the errors of the predictions.

$RMSE = \sqrt{\frac{1}{n} \sum_{i=1}^{n} (y_i - \hat{y}}_i)^2$

Kemudian dari **Root Mean Squared Error** kita juga mendapatkan rata-rata kesalahan prediksi sebesar 58.17674920907911. Angka ini merupakan angka yang kecil dari error yang di alami model. Untuk melihat seberapa performanya mari kita lihat dengan R-Squared atau yang sering di sebut dengan uji determinasi

### Coefficient of Determination atau R-squared ($R^2$)

$R^{2} = 1 - \frac{SS_{res}}{SS_{tot}}$


$SS_{res} =  \sum_{i=1}^{n}(y_i - f(x_i))^2$


$SS_{tot} =  \sum_{i=1}^{n}(y_i - \bar{y})^2$

Performa model ternyata R_Squared: 0.9899554134880288. Model yang digunakan memiliki nilai R-Squared yang begitu besar atau setara dengan 98% artinya model memiliki keakuratan sebesar 98% dalam melakukan prediksi benar

#### Note
- Semakin dekat nilai `R2` dengan 1 maka model semakin baik
- Semakin dekat nilai `R2` dengan -1 maka model semakin buruk
