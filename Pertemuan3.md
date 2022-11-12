# Modul 3 - Pengkondisian <b>If Else, Nested If dan Switch Case</b>
Tujuan Pembelajaran:
- Mahasiswa dapat memahami konsep pengkondisian
- Mahasiswa dapat memahami cara penggunaan pengkondisian
## 1. Persiapan:
- Buka aplikasi Visual Studio Code
- Buatlah file baru dengan nama `pertemuan3.php`
- Ketikkan kode program berikut:
```php
<?php
echo "Pengkondisian";
?>
```
- Simpan file tersebut dengan nama `pertemuan3.php`
- Buka terminal Visual Studio Code
- Ketikkan command:
```
php pertemuan3.php
```
- Output yang dihasilkan adalah sebagaiberikut:
```
Pengkondisian
```
## 2. Materi:
### 2.1 Pengkondisian
![GambarKondisi](https://glints.com/id/lowongan/wp-content/uploads/2021/06/blogthecenterforsalesstrategy.jpeg)
Pengkondisian adalah suatu pernyataan yang digunakan untuk mengeksekusi suatu pernyataan jika kondisi yang ditentukan terpenuhi. Pernyataan yang dieksekusi jika kondisi terpenuhi disebut dengan pernyataan `true`. Pernyataan yang dieksekusi jika kondisi tidak terpenuhi disebut dengan pernyataan `false`. Pernyataan `true` dan `false` dapat berupa pernyataan yang berupa satu baris maupun lebih dari satu baris.
#### Pseudocode
```
if (kondisi) {
    pernyataan true / benar
} else {
    pernyataan false / salah
}
```
#### Flowchart
![Pengkondisian](https://www.testingdocs.com/wp-content/uploads/If-Example-Flowchart.png)

### 2.2 If Else
Pengkondisian if else digunakan untuk mengeksekusi suatu kode program jika suatu kondisi terpenuhi. Jika kondisi tidak terpenuhi, maka kode program yang akan dieksekusi adalah kode program yang ada di dalam blok else.
```php
<?php
$nilai = 70;
if ($nilai >= 60) {
    echo "Nilai Anda $nilai, Anda Lulus";
} else {
    echo "Nilai Anda $nilai, Anda Tidak Lulus";
}
?>
```
Output yang dihasilkan adalah sebagai berikut:
```
Nilai Anda 70, Anda Lulus
```
### 2.3 Nested If
Pengkondisian nested if digunakan untuk mengeksekusi suatu kode program jika suatu kondisi terpenuhi. Jika kondisi tidak terpenuhi, maka kode program yang akan dieksekusi adalah kode program yang ada di dalam blok else. Pada pengkondisian nested if, kita dapat menambahkan kondisi lagi di dalam blok if.
```php
<?php
$nilai = 70;
if ($nilai >= 60) {
    if ($nilai >= 80) {
        echo "Nilai Anda $nilai, Anda Lulus dengan nilai A";
    } else {
        echo "Nilai Anda $nilai, Anda Lulus dengan nilai B";
    }
} else {
    echo "Nilai Anda $nilai, Anda Tidak Lulus";
}
?>
```
Output yang dihasilkan adalah sebagai berikut:
```
Nilai Anda 70, Anda Lulus dengan nilai B
```
### 2.4 SwitchCase
Switch case merupakan sebuah kondisi dimana kondisi yang terpenuhi nanti akan dilempar pada setiap casenya. Switch biasanya digunakan untuk kondisi yang cukup banyak. Perbedaan penggunaan switch case dangan if adalah switch case digunakan untuk banyak kondisi sedangkan untuk if digunakan untuk satu kondisi. bentuk umum dari switch case adalah sebagai berikut:

```
pilihan = 2;
switch(pilihan) {
    case 1:
        echo "Anda memilih 1";
        break;
    case 2:
        echo "Anda memilih 2";
        break;
    default:
        echo "Pilihan yang anda masukkan tidak tersedia";
    break;
}
```
## 3. Praktikum
- Buatlah program untuk menentukan apakah suatu bilangan merupakan bilangan ganjil atau genap.
```php
<?php
$bilangan = 10;
if ($bilangan % 2 == 0) {
    echo "$bilangan adalah bilangan genap";
} else {
    echo "$bilangan adalah bilangan ganjil";
}
?>
```
Output yang dihasilkan adalah sebagai berikut:
```
10 adalah bilangan genap
```
- Buatlah program untuk menentukan apakah suatu bilangan merupakan bilangan positif atau negatif.
```php
<?php
$bilangan = -10;
if ($bilangan > 0) {
    echo "$bilangan adalah bilangan positif";
} else {
    echo "$bilangan adalah bilangan negatif";
}
?>
```
Output yang dihasilkan adalah sebagai berikut:
```
-10 adalah bilangan negatif
```
### 4. Tugas Praktikum
- Terdapat sebuah bus yang memiliki kapasitas penumpang sebanyak 50 orang. bus tersebut akan berangkat jika jumlah penumpang sudah mencapai 50 orang. Buatlah program untuk menentukan apakah bus tersebut akan berangkat atau tidak.
- Dalam sebuah kelas terdapat 10 laki-laki dan 15 perempuan. Buatlah program untuk menentukan apakah jumlah laki-laki dan perempuan dalam kelas tersebut sama atau tidak.
- Dalam sebuah stadion terdapat tempat parkir sepeda motor, biaya untuk memarkir kendaraan mobil adalah Rp. 5000,- dan untuk sepeda motor adalah Rp. 3000,-.  Namun setiap kendaraan memiliki jenis plat nomor, jika kendaraan memiliki plat nomor yang tergolong genap maka biaya parkirnya akan diberikan diskon sebesar 10%. Buatlah program untuk menentukan biaya parkir kendaraan yang akan datang.
- Dalam sebuah toko terdapat 3 barang, yaitu barang A, barang B, dan barang C. Barang A memiliki harga Rp. 10000,-, barang B memiliki harga Rp. 15000,-, dan barang C memiliki harga Rp. 20000,-. Jika pembeli membeli barang A dan barang B maka akan mendapatkan diskon sebesar 10%. Jika pembeli membeli barang A, barang B, dan barang C maka akan mendapatkan diskon sebesar 20%. Buatlah program untuk menentukan total harga yang harus dibayar oleh pembeli.
- Dari beberapa mahasiswa yang mengikuti ujian, terdapat 5 mahasiswa yang mendapatkan nilai 90 dan terdapat mahasiswa yang mendapatkan nilai 50. Semua mahasiswa yang mendapatkan nilai 90 akan mendapatkan hadiah, sedangkan mahasiswa yang mendapatkan nilai 50 akan mendapatkan hukuman. Buatlah program untuk menentukan apakah mahasiswa tersebut mendapatkan hadiah atau hukuman.
## 4. Referensi
- [Pengkondisian](https://www.petanikode.com/php-pengkondisian/)
- [If Else](https://www.petanikode.com/php-if-else/)
- [Nested If](https://www.petanikode.com/php-nested-if/)
- [Pengkondisian If Else](https://www.testingdocs.com/php/pengkondisian-if-else/)
