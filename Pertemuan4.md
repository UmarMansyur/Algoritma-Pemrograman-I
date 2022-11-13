# Modul 4 - Perulangan For
Tujuan Pembelajaran:
- Mahasiswa mampu memahami konsep perulangan
- Mahasiswa mampu memahami cara penggunaan perulangan
- Mahasiswa mampu memahami konsep dan cara penggunaan perulangan for
## 1. Persiapan:
- Buka aplikasi Visual Studio Code
- Buatlah file baru dengan nama `pertemuan4.php`
- Ketikkan kode program berikut:
```php
<?php
echo "Perulangan";
?>
```
- Simpan file tersebut dengan nama `pertemuan4.php`
- Buka terminal Visual Studio Code
- Ketikkan command:
```
php pertemuan4.php
```
- Output yang dihasilkan adalah sebagai berikut:
```
Perulangan
```
## 2. Materi:
### 2.1 Perulangan
Perulangan adalah suatu pernyataan yang digunakan untuk mengeksekusi suatu pernyataan berulang kali. Pernyataan yang dieksekusi berulang kali disebut dengan pernyataan `loop`.
#### Pseudocode
```
for (inisialisasi; kondisi; increment) {
    pernyataan
}
```
#### Flowchart
![Perulangan](https://www.testingdocs.com/wp-content/uploads/For-Loop-Flowchart.png)
### 2.2 For
Perulangan for digunakan untuk mengeksekusi suatu kode program berulang kali. Pada perulangan for, kita dapat menentukan jumlah perulangan yang akan dieksekusi.
```php
<?php
for ($i = 0; $i < 5; $i++) {
    echo "Perulangan ke-$i";
}
?>
```
#### Pseudocode
```
for (inisialisasi; kondisi; increment) {
    pernyataan
}
```
#### Flowchart
![Perulangan For](https://www.testingdocs.com/wp-content/uploads/For-Loop-Flowchart.png)
#### Penjelasan
- `for` merupakan kata kunci untuk perulangan for
- `($i = 0; $i < 5; $i++)` merupakan bagian inisialisasi, kondisi, dan increment
- `$i = 0` merupakan inisialisasi, dimana kita menginisialisasi variabel `$i` dengan nilai 0
- `$i < 5` merupakan kondisi, dimana kita menentukan kondisi perulangan. Pada contoh di atas, perulangan akan terus berjalan selama nilai variabel `$i` kurang dari 5
- `$i++` merupakan increment, dimana kita menentukan increment variabel `$i`. Pada contoh di atas, nilai variabel `$i` akan bertambah 1 setiap perulangan
- `echo "Perulangan ke-$i";` merupakan pernyataan yang akan dieksekusi selama perulangan berjalan
### 2.3 Contoh Kasus
#### Contoh Kasus 1
Tampilkan deret bilangan 1 sampai 10
```php
<?php
for ($i = 1; $i <= 10; $i++) {
    echo "$i ";
}
?>
```
#### Contoh Kasus 2
Tampilkan deret bilangan 10 sampai 1
```php
<?php
for ($i = 10; $i >= 1; $i--) {
    echo "$i ";
}
?>
```
#### Contoh Kasus 3
Tampilkan deret bilangan 1 sampai 10 dengan kelipatan 2
```php
<?php
for ($i = 1; $i <= 10; $i += 2) {
    echo "$i ";
}
?>
```
#### Contoh Kasus 4
Tampilkan deret bilangan 10 sampai 1 dengan kelipatan 2
```php
<?php   
for ($i = 10; $i >= 1; $i -= 2) {
    echo "$i ";
}
?>
```
### Kegiatan Praktikum
1. Buatlah program untuk menampilkan deret bilangan genap
```php
<?php
for ($i = 1; $i <= 10; $i++) {
    if ($i % 2 == 0) {
        echo "$i ";
    }
}
?>
```
Keterangan:
- `$i` merupakan variabel yang digunakan untuk menampung nilai perulangan
- `$i % 2 == 0` merupakan syarat untuk menentukan bilangan genap
2. Buatlah program untuk menampilkan bilangan yang habis dibagi 3
```php
<?php
for ($i = 1; $i <= 10; $i++) {
    if ($i % 3 == 0) {
        echo "$i ";
    }
}
?>
```
Keterangan:
- `$i` merupakan variabel yang digunakan untuk menampung nilai perulangan
- `$i % 3 == 0` merupakan syarat untuk menentukan bilangan yang habis dibagi 3
3. Buatlah bintang segitiga
```php
<?php
for ($i = 1; $i <= 5; $i++) {
    for ($j = 1; $j <= $i; $j++) {
        echo "*";
    }
    echo "\n";
}
?>
```
Output:
```
*
**
***
****
*****
```
Keterangan:
- `$i` merupakan variabel yang digunakan untuk menampung nilai perulangan
- `$j` merupakan variabel yang digunakan untuk menampung nilai perulangan
- `$j <= $i` merupakan syarat untuk menentukan jumlah bintang yang akan ditampilkan
- `echo "*";` merupakan pernyataan yang akan dieksekusi selama perulangan berjalan
- `echo "\n";` merupakan pernyataan untuk membuat baris

Dari kode program bintang segitiga di atas, dapat kita ketahui bahwa for juga dapat memiliki for di dalamnya. for yang berada di dalam akan di eksekusi terlebih dahulu, kemudian for yang berada di luar akan di eksekusi. kita dapat membayangkan pohon pemfaktoran. for yang di luar dapat di ilustrasikan sebagai root dari pohon, sedangkan for yang berada di dalamnya dapat di ilustrasikan sebagai anak dari root.
Kode program yang menggunakan for yang berada di dalam for disebut dengan <i>nested for</i>.
### 3. Tugas Praktikum
1. Buatlah program untuk menampilkan deret bilangan ganjil
2. Buatlah program untuk menampilkan bilangan yang habis dibagi 5
3. Buatlah bintang segitiga terbalik
4. Buatlah bintang segitiga sama kaki
5. Buatlah bintang segitiga sama kaki terbalik
6. Buatlah bintang segitiga sama kaki terbalik dengan angka
8. Buatlah pola seperti gambar berikut
```
1
2 3
4 5 6
7 8 9 10
11 12 13 14 15
```
9. Buatlah pola seperti gambar berikut
```
1 * # * 5 # 7 * # *
```
10. Buatlah pola bintang seperti gambar berikut:
```
      *
     * *
*****   *****
 *    *    *
  * *   * *
   *     *
```
11. Buatlah pola bintang seperti Logo NAZI:
```
****************
*
****************
               *
****************
```
12. Buatlah pola bintang angka sesuai nim !










