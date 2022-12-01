# Modul 5 - Perulangan while dan do While
Tujuan Pembelajaran:
- Mahasiswa mampu memahami konsep perulangan
- Mahasiswa mampu memahami cara penggunaan perulangan
- Mahasiswa mampu memahami konsep dan cara penggunaan perulangan while
## 1. Persiapan:
- Buka aplikasi Visual Studio Code
- Buatlah file baru dengan nama `pertemuan5.php`
- Ketikkan kode program berikut:
```php
<?php
echo "Perulangan While";
?>
```
- Simpan file tersebut dengan nama `pertemuan5.php`
- Buka terminal Visual Studio Code
- Ketikkan command:
```
php pertemuan5.php
```
- Output yang dihasilkan adalah sebagai berikut:
```
Perulangan While
```
## 2. Materi:
### 2.1 Perulangan While
While adalah perulangan yang akan terus berjalan selama kondisi yang ditentukan bernilai true. Pada perulangan while, kita tidak perlu menentukan jumlah perulangan yang akan dieksekusi.
#### Pseudocode
```
while (kondisi) {
    pernyataan
}
```
#### Flowchart
![Perulangan While](https://www.testingdocs.com/wp-content/uploads/While-Loop-Flowchart.png)
#### Kode Program
```php
<?php
$i = 0;
while ($i < 5) {
    echo "Perulangan ke-$i";
    $i++;
}
?>
```
Keterangan:
- `while` merupakan kata kunci untuk perulangan while
- `(kondisi)` merupakan kondisi perulangan. Pada contoh di atas, perulangan akan terus berjalan selama nilai variabel `$i` kurang dari 5
- `{pernyataan}` merupakan pernyataan yang akan dieksekusi selama kondisi bernilai true

### 2.2 Perulangan Do While
Do While adalah perulangan yang akan terus berjalan selama kondisi yang ditentukan bernilai true. Perbedaan dengan perulangan while adalah, perulangan do while akan dieksekusi minimal sekali, walaupun kondisi bernilai false.
#### Pseudocode
```
do {
    pernyataan
} while (kondisi);
```
#### Flowchart
![Perulangan Do While](https://www.testingdocs.com/wp-content/uploads/Do-While-Loop-Flowchart.png)
#### Kode Program
```php
<?php
$i = 0;
do {
    echo "Perulangan ke-$i";
    $i++;
} while ($i < 5);
?>
```
Keterangan:
- `do` merupakan kata kunci untuk perulangan do while
- `{pernyataan}` merupakan pernyataan yang akan dieksekusi selama kondisi bernilai true
- `while` merupakan kata kunci untuk perulangan while
- `(kondisi)` merupakan kondisi perulangan. Pada contoh di atas, perulangan akan terus berjalan selama nilai variabel `$i` kurang dari 5
### 2.3 Perbedaan While dan Do While
- Perbedaan antara perulangan while dan do while adalah, perulangan do while akan dieksekusi minimal sekali, walaupun kondisi bernilai false. Sedangkan perulangan while tidak akan dieksekusi sama sekali jika kondisinya bernilai false.
- Perulangan while lebih efisien daripada perulangan do while karena perulangan do while akan dieksekusi minimal sekali, walaupun kondisinya bernilai false.
## 3. Praktikum:
1. Buatlah program untuk menampilkan bilangan genap dari 1 sampai 10 menggunakan perulangan while dab do while! <br/>
jawab: <br/>
```php
<?php
$i = 1; 
while ($i <= 10) {
    if ($i % 2 == 0) {
        echo "$i ";
    }
    $i++;
}
echo "\n";
$i = 1;
do {
    if ($i % 2 == 0) {
        echo "$i ";
    }
    $i++;
} while ($i <= 10);
?>
```
### 4. Tugas Praktikum
1. Buatlah program pendaftaran mahasiswa baru dengan ketentuan sebagai berikut:
- Nama lengkap
- NIM
- Jenis kelamin
- Alamat
- Jurusan
- Fakultas
- IPK
- Jumlah SKS yang sudah ditempuh
- Jumlah SKS yang akan ditempuh
- Jumlah SKS yang harus ditempuh
- Jumlah SKS yang sudah ditempuh harus lebih besar dari 0
- Jumlah SKS yang akan ditempuh harus lebih besar dari 0
- Jumlah SKS yang harus ditempuh harus lebih besar dari 0
- Jumlah SKS yang akan ditempuh harus lebih kecil dari jumlah SKS yang harus ditempuh
- Jumlah SKS yang akan ditempuh harus lebih kecil dari 24
- IPK harus lebih besar dari 0
- IPK harus lebih kecil dari 4
- Jika semua syarat terpenuhi, maka mahasiswa tersebut dinyatakan lulus
- Jika tidak, maka mahasiswa tersebut dinyatakan tidak lulus
- Tampilkan hasilnya
2. Buatlah program untuk menampilkan bilangan prima dari 1 sampai 100 menggunakan perulangan while dan do while!
3. Buatlah program penjualan dengan ketentuan sebagai berikut:
- Nama barang
- Harga barang
- Jumlah barang
- Total harga
- Jumlah uang yang dibayarkan
- Kembalian
- Jumlah uang yang dibayarkan harus lebih besar dari total harga
- Jumlah uang yang dibayarkan harus lebih besar dari 0
- Jumlah barang harus lebih besar dari 0
- Jika semua syarat terpenuhi, maka tampilkan total harga, jumlah uang yang dibayarkan, dan kembalian
- Jika tidak, maka tampilkan pesan "Transaksi gagal"
- Diskon 10% jika jumlah barang lebih dari 10
- Diskon 20% jika jumlah barang lebih dari 20
- Diskon 30% jika jumlah barang sama dengan nim anda
4. Buatlah progam untuk penyewaan mobil dengan ketentuan sebagai berikut:
- Nama peminjam
- Nama mobil
- Jumlah hari
- Total harga
- Jumlah uang yang dibayarkan
- Kembalian
- Jumlah uang yang dibayarkan harus lebih besar dari total harga
- Jumlah uang yang dibayarkan harus lebih besar dari 0
- Jumlah hari harus lebih besar dari 0
- Jika semua syarat terpenuhi, maka tampilkan total harga, jumlah uang yang dibayarkan, dan kembalian
- Jika tidak, maka tampilkan pesan "Transaksi gagal"
- Diskon 10% jika jumlah hari lebih dari 10
- Diskon 20% jika jumlah hari lebih dari 20
- Harga mobil:
    - Avanza = 200000
    - Xenia = 250000
    - Innova = 300000
    - Fortuner = 350000
5. Buatlah program untuk menghitung nilai rata-rata dari 3 nilai mahasiswa dengan ketentuan sebagai berikut:
- Nama mahasiswa
- Nilai 1
- Nilai 2
- Nilai 3
- Nilai rata-rata
- Nilai 1 harus lebih besar dari 0
- Nilai 2 harus lebih besar dari 0
- Nilai 3 harus lebih besar dari 0
- Jika semua syarat terpenuhi, maka tampilkan nilai rata-rata
- Jika tidak, maka tampilkan pesan "Nilai tidak valid"
6. Buatlah program untuk menghitung biaya bahan bakar mobil, jika diketahui:
- Jarak tempuh
- Jumlah bahan bakar yang digunakan
- Harga bahan bakar
Mobil yang digunakan adalah Avanza, dengan ketentuan sebagai berikut:
- Jarak tempuh harus lebih besar dari 0
- Jumlah bahan bakar yang digunakan harus lebih besar dari 0
- Harga bahan bakar harus lebih besar dari 0
- Jika semua syarat terpenuhi, maka tampilkan biaya bahan bakar
- Jika tidak, maka tampilkan pesan "Nilai tidak valid"
- Jarak tempuh = 100 km
- Jumlah bahan bakar yang digunakan = 1 liter
- Harga bahan bakar = 5000
- Jika biaya bahan bakar lebih dari 100000, maka tampilkan pesan "Biaya bahan bakar mahal" sehingga biaya mendapatkan diskon dari pemerintah berdasarkan nim belakang
7. Jika pada suatu umar sedang membeli buku seharga 50000, buku tersebut ternyata tidak sesuai dengan keinginannya, maka dia memutuskan untuk mengembalikannya. Namun, dia tidak tahu berapa banyak uang yang harus dibayarkan kepada penjual. Bantulah dia untuk mengetahui berapa banyak uang yang harus dibayarkan kepada penjual! 



