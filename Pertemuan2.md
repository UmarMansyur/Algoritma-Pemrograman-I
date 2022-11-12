# Modul 2 - Tipe Data, Variabel dan Operator
Tujuan Pembelajaran:
- Mahasiswa dapat memahami konsep tipe data, variabel dan operator
- Mahasiswa dapat memahami cara penggunaan tipe data, variabel dan operator
## 1. Persiapan:
- Buka aplikasi Visual Studio Code
- Buatlah file baru dengan nama `pertemuan2.php`
- Ketikkan kode program berikut:
```php
<?php
echo "Tipe Data, Variabel, dan Operator";
?>
```
- Simpan file tersebut dengan nama `pertemuan2.php`
- Buka terminal Visual Studio Code
- Ketikkan command:
```
php pertemuan2.php
```
- Jika muncul tulisan seperti berikut, maka program PHP telah berhasil dijalankan
```
Tipe Data, Variabel, dan Operator
```
## 2. Materi:
### 2.1 Tipe Data
Tipe data adalah jenis data yang digunakan untuk menyimpan nilai. Tipe data dapat berupa angka, teks, dan lain-lain. Tipe data juga dapat berupa tipe data khusus seperti tipe data boolean, array, dan object. Tipe data dapat digunakan untuk menentukan jenis data apa yang akan disimpan dalam variabel.
#### 2.1.1 Tipe Data Boolean
Tipe data boolean hanya memiliki dua nilai, yaitu `true` dan `false`. Nilai `true` berarti benar, sedangkan nilai `false` berarti salah. Tipe data boolean sering digunakan untuk menentukan apakah suatu kondisi terpenuhi atau tidak.
```php
<?php
$benar = true;
$salah = false;
?>
```
#### 2.1.2 Tipe Data Integer
Tipe data integer adalah tipe data yang digunakan untuk menyimpan bilangan bulat. Tipe data integer memiliki nilai maksimum sebesar 2,147,483,647. Jika nilai yang disimpan melebihi nilai maksimum, maka nilai akan kembali ke nilai minimum.
```php
<?php
$bilangan_bulat = 123;
?>
```
#### 2.1.3 Tipe Data Float
Tipe data float adalah tipe data yang digunakan untuk menyimpan bilangan desimal. Tipe data float memiliki nilai maksimum sebesar 1.7976931348623E+308. Jika nilai yang disimpan melebihi nilai maksimum, maka nilai akan kembali ke nilai minimum.
```php
<?php
$bilangan_desimal = 123.45;
?>
```
#### 2.1.4 Tipe Data String
Tipe data string adalah tipe data yang digunakan untuk menyimpan teks. Tipe data string dapat berupa teks yang berisi angka, huruf, dan simbol. Tipe data string dapat berupa teks yang berisi satu kata, satu kalimat, atau lebih dari satu kalimat.
```php
<?php
$teks = "Belajar PHP";
?>
```
#### 2.1.5 Tipe Data Array
Tipe data array adalah tipe data yang digunakan untuk menyimpan lebih dari satu nilai. Tipe data array dapat digunakan untuk menyimpan nilai-nilai yang memiliki tipe data yang sama maupun berbeda. Tipe data array dapat digunakan untuk menyimpan nilai-nilai yang memiliki tipe data yang sama maupun berbeda. Tipe data array dapat digunakan untuk menyimpan nilai-nilai yang memiliki tipe data yang sama maupun berbeda.
```php
<?php
$angka = array(1, 2, 3, 4, 5);
$teks = array("satu", "dua", "tiga", "empat", "lima");
$campuran = array(1, "dua", 3, "empat", 5);
?>
```
#### 2.1.6 Tipe Data Object
Tipe data object adalah tipe data yang digunakan untuk menyimpan nilai-nilai yang memiliki tipe data yang sama maupun berbeda. Tipe data object dapat digunakan untuk menyimpan nilai-nilai yang memiliki tipe data yang sama maupun berbeda. Tipe data object dapat digunakan untuk menyimpan nilai-nilai yang memiliki tipe data yang sama maupun berbeda.
```php
<?php
class Mobil {
    public $merk;
    public $warna;
    public $harga;
}
$mobil = new Mobil();
$mobil->merk = "Toyota";
$mobil->warna = "Putih";
$mobil->harga = "100000000";
?>
```
Tipe data array akan dibahas lebih lanjut pada algoritma pemrograman II sedangkan untuk tipe data objek akan dijelaskan pada materi OOP (Semester III).
### 2.2 Variabel
Variabel adalah sebuah wadah yang dapat digunakan untuk menyimpan data. Variabel dapat digunakan untuk menyimpan data berupa angka, huruf, dan sebagainya. Variabel dapat digunakan untuk menyimpan data sementara atau data yang akan digunakan berulang kali. <br/>
Pada PHP, variabel diawali dengan tanda `$`. <br/>
Contoh:
```php
<?php
$nama = "John Doe";
$umur = 20;
$tinggi = 170.5;
$menikah = false;
?>
```
Keterangan:
- `$nama` adalah variabel yang menyimpan data berupa string
- `$umur` adalah variabel yang menyimpan data berupa integer
- `$tinggi` adalah variabel yang menyimpan data berupa float
- `$menikah` adalah variabel yang menyimpan data berupa boolean

Dalam PHP, variabel bersifat case-sensitive. Artinya, penamaan variabel bersifat sensitif terhadap huruf besar dan huruf kecil. <br/>
Contoh:
```php
<?php
$nama = "Muhammad Umar Mansyur";
$Nama = "Ali Rahman";
$NAMA = "Moh. Qoming Zaki";
echo $nama; // Muhammad Umar Mansyur
echo $Nama; // Ali Rahman
echo $NAMA; // Moh. Qoming Zaki
?>
```
Variabel di bahasa pemrograman PHP bersifat dinamis. Artinya, variabel dapat digunakan untuk menyimpan data berupa tipe data apapun. PHP tergolong kepada bahasa pemrograman yang memiliki tipe data yang dinamis. <br/>
### 2.3 Operator
Operator adalah simbol yang digunakan untuk melakukan operasi matematika atau logika. <br/>
Pada PHP, operator dapat berupa: <br/>
- Aritmatika
- Penugasan
- Perbandingan
- Logika
- Increment/Decrement
- String
#### 2.3.1 Operator Aritmatika
Operator aritmatika digunakan untuk melakukan operasi matematika. <br/>
Contoh:
```php
<?php
$x = 10;
$y = 5;
echo $x + $y; // 15
echo $x - $y; // 5
echo $x * $y; // 50
echo $x / $y; // 2
echo $x % $y; // 0
?>
```
#### 2.3.2 Operator Penugasan
Operator penugasan digunakan untuk menugaskan nilai ke dalam variabel. <br/>
Contoh:
```php
<?php
$x = 10;
$y = 5;
$x += $y; // $x = $x + $y
$x -= $y; // $x = $x - $y
$x *= $y; // $x = $x * $y
$x /= $y; // $x = $x / $y
$x %= $y; // $x = $x % $y
?>
```
#### 2.3.3 Operator Perbandingan
Operator perbandingan digunakan untuk membandingkan dua buah nilai. <br/>
Contoh:
```php
<?php
$x = 10;
$y = 5;
echo $x == $y; // false
echo $x != $y; // true
echo $x > $y; // true
echo $x < $y; // false
echo $x >= $y; // true
echo $x <= $y; // false
?>
```
#### 2.3.4 Operator Logika
Operator logika digunakan untuk menggabungkan dua buah kondisi. <br/>
Contoh:
```php
<?php
$x = 10;
$y = 5;
echo $x == 10 && $y == 5; // true
echo $x == 10 || $y == 5; // true
echo !$x == 10; // false
?>
```
#### 2.3.5 Operator Increment/Decrement
Operator increment/decrement digunakan untuk menambahkan atau mengurangi nilai variabel. <br/>
Contoh:
```php
<?php
$x = 10;
$y = 5;
echo ++$x; // 11
echo --$y; // 4
echo $x++; // 11
echo $y--; // 5
?>
```
#### 2.3.6 Operator String
Operator string digunakan untuk menggabungkan dua buah string. <br/>
Contoh:
```php
<?php
$namaDepan = "John";
$namaBelakang = "Doe";
echo $namaDepan . " " . $namaBelakang; // John Doe
?>
```
### 3. Praktikum
#### 3.1 Membuat Program Sederhana
Buatlah program sederhana untuk menghitung luas persegi panjang. <br/>
Contoh:
```php
<?php
$panjang = 10;
$lebar = 5;
$luas = $panjang * $lebar;
echo "Luas persegi panjang adalah " . $luas;
?>
```
#### 3.2 Membuat Program Sederhana dengan Inputan
Buatlah program sederhana untuk menghitung luas persegi panjang dengan inputan dari user meggunakan terminal. <br/>
Contoh:
```php
<?php
echo "Masukkan panjang: ";
$panjang = trim(fgets(STDIN));
echo "Masukkan lebar: ";
$lebar = trim(fgets(STDIN));
$luas = $panjang * $lebar;
echo "Luas persegi panjang adalah " . $luas;
?>
```
```php
$uts = trim(fgets(STDIN));
```
Keterangan: <br/>
- `trim()` digunakan untuk menghapus spasi di awal dan akhir string
- `fgets(STDIN)` digunakan untuk membaca inputan dari user
#### 3.3 Membuat Program Sederhana dengan Inputan dan Validasi
Buatlah program sederhana untuk menghitung luas persegi panjang dengan inputan dari user meggunakan terminal dan validasi inputan. <br/>
Contoh:
```php
<?php
echo "Masukkan panjang: ";
$panjang = is_numeric(trim(fgets(STDIN))) ? trim(fgets(STDIN)) : 1; 
echo "Masukkan lebar: ";
$lebar = is_numeric(trim(fgets(STDIN))) ? trim(fgets(STDIN)) : 1;
$luas = $panjang * $lebar;
echo "Luas persegi panjang adalah " . $luas;
?>
```
#### 3.3 Membuat Program untuk Menghitung Nilai Akhir
Buatlah program untuk menghitung nilai akhir dari nilai UTS, UAS, dan Tugas. <br/>
Contoh:
```php
<?php
echo "Masukkan nilai UTS: ";
$uts = is_numeric(trim(fgets(STDIN))) ? trim(fgets(STDIN)) : 1;
echo "Masukkan nilai UAS: ";
$uas =is_numeric(trim(fgets(STDIN))) ? trim(fgets(STDIN)) : 1;
echo "Masukkan nilai Tugas: ";
$tugas = is_numeric(trim(fgets(STDIN))) ? trim(fgets(STDIN)) : 1;
$nilaiAkhir = (0.3 * $uts) + (0.3 * $uas) + (0.4 * $tugas);
echo "Nilai akhir adalah " . $nilaiAkhir;
?>
```
## 4. Tugas Praktikum:
1. Buatlah program untuk menghitung luas lingkaran. <br/>
2. Buatlah program sederhana untuk menghitung luas persegi panjang dengan menggunakan PHP. <br/>
3. Buatlah program sederhana untuk menghitung luas segitiga dengan menggunakan PHP. <br/>
4. Buatlah program sederhana untuk menghitung luas trapesium dengan menggunakan PHP. <br/>
5. Buatlah program sederhana untuk menghitung luas jajar genjang dengan menggunakan PHP. <br/>
6. Buatlah program sederhana untuk menghitung luas belah ketupat dengan menggunakan PHP. <br/>
7. Buatlah program sederhana untuk menghitung luas layang-layang dengan menggunakan PHP. <br/>
8. Buatlah program sederhana untuk menghitung luas bola dengan menggunakan PHP. <br/>
9. Buatlah program sederhana untuk menghitung luas kubus dengan menggunakan PHP. <br/>
10. Buatlah program sederhana untuk menghitung luas balok dengan menggunakan PHP. <br/>
11. Buatlah program sederhana untuk menghitung luas tabung dengan menggunakan PHP. <br/>
12. Buatlah program sederhana untuk menghitung luas kerucut dengan menggunakan PHP. <br/>
13. Buatlah program sederhana untuk menghitung luas prisma segitiga dengan menggunakan PHP. <br/>
14. Buatlah program inputan tentang biodata diri. <br/>
15. Buatlah program sederhana untuk menghitung luas limas segitiga dengan menggunakan PHP. <br/>
16. Buatlah program tentang penjualan makanan, dimana user dapat menampilkan menu masakan yang dimasukkan dan dapat mengetahui harga makanan yang dibeli. <br/>
17. Buatlah program tentang pengisian bom bensin dengan jenis bahan bakar yang berbeda. untuk pertamax 95, pertamax 97, pertamax 99, pertalite, premium, solar, dan bio solar. Masing-masing jenis bahan bakar memiliki harga yang berbeda. <br/>
18. asumsikan bahwa harga dari 3 bolpen adalah 5000. sedangkan harga dari 1 penggaris adalah 2000. Buatlah program untuk menghitung total harga dari 3 bolpen dan 1 penggaris. <br/>
19. Dalam permainan catur, setiap bidak memiliki nilai yang berbeda. Bidak yang paling tinggi adalah raja, sedangkan yang paling rendah adalah pion. Buatlah program untuk menghitung nilai dari 2 buah bidak yang dimasukkan oleh user. Dengan asumsi bahwa raja memiliki nilai 100, ratu 9, benteng 5, kuda 3, dan pion 1. <br/>
20. Buatlah program sederhana untuk menghitung luas kerucut dengan menggunakan PHP. <br/>
## Ketentuan: <br/>
- Gunakan inputan dari user menggunakan terminal. <br/>
- Gunakan operator aritmatika. <br/>
- NIM yang berakhiran ganjil maka mengerjakan soal ganjil, begitu juga sebaliknya. <br/>
- Lengkapi dengan validasi inputan. <br/>
- Tidak boleh menggunakan pengkondisian if. <br/>
- Program yang ditulis disalin ke carbon.now.sh dan dijadikan gambar. <br/>
- Output yang dihasilkan harus di screenshot, dan disertakan di setiap jawaban. <br/>
- Jenis kode program yang sama di anggap tidak mengerjakan. <br/>
- Setiap kode yang dibuat harus disertai penjelasan. <br/>
- Format laporan dapat di klik pada link berikut:
https://docs.google.com/document/d/13DdL1y43RwbF5HRPGseVgJWlYw1bdxgd/edit?usp=share_link&ouid=109974887201006898482&rtpof=true&sd=true