## Modul 1 - Pengantar Algoritma dan Pemrograman Dasar
Tujuan Pembelajaran: 
1. Mahasiswa dapat memahami konsep dasar algoritma dan pemrograman dasar.
2. Mahasiswa dapat mengenal bahasa pemrograman
3. Mahasiswa dapat mengetahui cara menginstall bahasa pemrograman PHP
4. Mahasiswa dapat mengetahui cara menginstall Visual Studio Code
### 1. Persiapan
Berikut adalah beberapa persiapan yang perlu dilakukan sebelum memulai praktikum: <br/>
1. Berdo'a <br/>
2. Mencari pengertian algoritma dan pemrograman <br/>
3. Mencari contoh dan bentuk implementasi algoritma dan pemrograman di kehidupan sehari hari<br/>
#### 1.1 Apa itu Algoritma?
Algoritma secara bahasa berasal dari kata algorism yang berarti perhitungan dalam bahasa arab. Dikutip dari buku Pengantar Ilmu Kriptografi Teori Analisis dan Implementasi karaya Dony Ariyus 2008 halaman 43 menyatakan bahwa algoritma sebenarnya diambil dari nama seorang tokoh matematikawan arab yaitu Muhammad Ibnu Musa Al-Khawarizmi, beliau adalah seorang tokoh yang menemukan simbol angka dalam matematika. Dari pengucapan nama beliaulah orang barat menyebut <i>Al-Khawarizmi</i> sebagai <i>Algorism</i>, <i>Algorithm</i> ataupun <i>Alogorismus</i>.Secara makna bahasa algoritma diartikan sebagai proses atau langkah-langkah yang harus dilakukan untuk mencapai suatu tujuan. Sedangkan secara istilah, algoritma adalah suatu langkah-langkah yang sistematis dan teratur untuk menyelesaikan suatu masalah.<br/>
Contohnya, semisal algoritma untuk membuat kopi, adapun langkah-langkahnya adalah sebagai berikut: <br/>
1. Siapkan alat dan bahan yang dibutuhkan <br/>
2. Masukkan kopi kedalam gelas <br/>
3. Masukkan gula kedalam gelas <br/>
4. Tuangkan air panas kedalam gelas <br/>
5. Aduk hingga rata <br/>
6. Nikmati kopi <br/>
Algortima di atas merupakan algoritma yang sederhana, namun algoritma yang lebih kompleks dapat ditemukan di berbagai bidang seperti: <br/>
1. Algoritma dalam bidang matematika <br/>
2. Algoritma dalam bidang ilmu komputer <br/>
3. Algoritma dalam bidang ilmu keuangan <br/>
4. Algoritma dalam bidang ilmu fisika <br/>
Contoh Algoritma dalam bidang matematika: <br/>
1. Algoritma Euclidean <br/>
2. Algoritma Euclidean Extended <br/>
3. Algoritma Euclidean Modulus <br/>
4. Algoritma Extended Euclidean <br/>
5. Algoritma Extended Euclidean Modulus <br/>
Contoh Algoritma dalam bidang ilmu komputer: <br/>
1. Algoritma Binary Search <br/>
2. Algoritma Bubble Sort <br/>
3. Algoritma Insertion Sort <br/>
4. Algoritma Selection Sort <br/>
5. Algoritma Merge Sort <br/>
Contoh Algoritma dalam bidang ilmu keuangan: <br/>
1. Algoritma Black-Scholes <br/>
2. Algoritma Monte Carlo <br/>
3. Algoritma Binomial <br/>
4. Algoritma Newton-Raphson <br/>
5. Algoritma Bisection <br/>
Contoh Algoritma dalam bidang ilmu fisika: <br/>
1. Algoritma Newton <br/>
2. Algoritma Euler <br/>
3. Algoritma Runge-Kutta <br/>
4. Algoritma Leapfrog <br/>
5. Algoritma Verlet <br/>
Dan masih banyak lagi contoh algoritma yang dapat ditemukan di berbagai bidang ilmu. Karena pengertian algoritma sangat luas, maka dalam praktikum ini akan dijelaskan secara singkat mengenai algoritma dalam bidang ilmu komputer. Dalam bidang ilmu komputer, algoritma memiliki bentuk umum sebagai berikut: <br/>
```
Input: suatu masukan yang diperlukan untuk menyelesaikan suatu masalah
Output: suatu keluaran yang dihasilkan dari suatu masalah
Proses: langkah-langkah yang harus dilakukan untuk menyelesaikan suatu masalah
```
Contoh algoritma dalam bidang ilmu komputer: <br/>
```
Input: suatu bilangan bulat positif
Output: suatu bilangan bulat positif
Proses:
1. Jika bilangan tersebut lebih besar dari 0 maka bilangan tersebut merupakan bilangan positif
2. Jika bilangan tersebut lebih kecil dari 0 maka bilangan tersebut merupakan bilangan negatif
3. Jika bilangan tersebut sama dengan 0 maka bilangan tersebut merupakan bilangan nol
```
#### 1.2 Apa itu Pemrograman?
Pemrograman adalah suatu proses untuk menulis program komputer. Program komputer adalah suatu kumpulan instruksi yang ditulis dalam suatu bahasa pemrograman yang dapat dijalankan oleh komputer. Pemrograman dapat dilakukan dengan menggunakan berbagai macam bahasa pemrograman, seperti: <br/>
``` 
1. C
2. C++
3. Java
4. Python
5. PHP
```
Dan masih banyak lagi bahasa pemrograman yang dapat digunakan untuk menulis program komputer. Pada praktikum ini akan dijelaskan mengenai pemrograman menggunakan bahasa PHP. <br/>
#### 1.3 Apa itu PHP ?
PHP adalah akronim dari <i>Hipertext Prepocessor</i>. Hipertext Prepocessor adalah bahasa skrip yang dapat digunakan untuk pengembangan web. PHP dapat digunakan untuk membuat website dinamis, seperti: <br/>
```
1. Website yang dapat diakses oleh banyak pengguna
2. Website yang dapat diakses oleh pengguna yang berbeda-beda
3. Website yang dapat diakses oleh pengguna yang berbeda-beda dan memiliki hak akses yang berbeda-beda
```
Contoh Penulisan PHP: <br/>
```
<?php
echo "Hello World";
// output yang dihasilkan adalah Hello World
?>
```
#### 1.4 Instalasi PHP
Untuk dapat menggunakan bahasa pemrograman PHP, maka diperlukan sebuah software yang dapat menjalankan bahasa pemrograman PHP. Software tersebut adalah <i>Web Server</i>. Web Server adalah sebuah software yang dapat menjalankan program PHP. Web Server yang umum digunakan adalah <i>Apache</i> dan <i>NginX</i>. Namun untuk versi PHP 7 ke atas, PHP dapat membuat server sendiri dengan menjalankan command:
```
php -S localhost:8000
```
PHP dapat didownload di <a href="https://www.php.net/downloads.php">https://www.php.net/downloads.php</a>. Pada praktikum ini akan dijelaskan mengenai instalasi PHP pada sistem operasi Windows. <br/>
Adapun langkah-langkah instalasi PHP pada sistem operasi Windows adalah sebagai berikut: <br/>
1. Download PHP di <a href="https://www.php.net/downloads.php">https://www.php.net/downloads.php</a> <br/>
2. Pilih versi PHP yang akan diinstall (Windows Downloads) <br/>
3. Pilih versi Thread Safe, ZIP <br/>
4. Ekstrak file yang telah diunduh <br/>
5. Pindahkan folder hasil ekstraksi ke C:\ <br/>
6. Buka Command Prompt <br/>
7. Ketikkan command: <br/>
```
cd C:\php
```
8. Ketikkan command: <br/>
```
php -v
```
9. Jika muncul tulisan seperti berikut, maka PHP telah berhasil diinstall <br/>
```
PHP 8.1.0 (cli) (built: Dec  1 2021 15:00:00) ( ZTS Visual C++ 2019 x64 )
Copyright (c) The PHP Group
Zend Engine v4.1.0, Copyright (c) Zend Technologies
```
10. Agar PHP dapat dikenali di Command Prompt, maka diperlukan sebuah perintah tambahan. Untuk menambahkan perintah tersebut, maka buka Command Prompt sebagai Administrator <br/>
11. Ketikkan command: <br/>
```
setx path "%path%;C:\php"
```
12. Jika muncul tulisan seperti berikut, maka perintah telah berhasil ditambahkan <br/>
```
SUCCESS: Specified value was saved.
```
#### 1.5 Instalasi Visual Studio Code
Visual Studio Code adalah sebuah text editor yang dapat digunakan untuk menulis program PHP. Visual Studio Code dapat didownload di <a href="https://code.visualstudio.com/download">https://code.visualstudio.com/download</a>. Pada praktikum ini akan dijelaskan mengenai instalasi Visual Studio Code pada sistem operasi Windows. <br/>
Adapun langkah-langkah instalasi Visual Studio Code pada sistem operasi Windows adalah sebagai berikut: <br/>
1. Download Visual Studio Code di <a href="https://code.visualstudio.com/download">https://code.visualstudio.com/download</a> <br/>
2. Pilih versi yang sesuai dengan sistem operasi windows.  <br/>
3. Klik aplikasi yang telah diunduh <br/>
4. Ikuti langkah-langkah instalasi yang dimunculkan <br/>
### 1.6 Memulai Membuat Program PHP
Pada praktikum ini akan dijelaskan mengenai cara membuat program PHP. <br/>
1. Buka Visual Studio Code <br/>
2. Klik File -> New File <br/>
3. Ketikkan kode program PHP <br/>
```
<?php
echo "Hello World";
?>
```
4. Simpan file dengan nama <i>hello.php</i> <br/>
5. Buka terminal Visual Studio Code <br/>
6. Ketikkan command: <br/>
```
php hello.php
```
7. Jika muncul tulisan seperti berikut, maka program PHP telah berhasil dijalankan <br/>
```
Hello World
```
### 2. Tugas Praktikum
1. Buatlah video tutorial mengenai cara instalasi PHP dan Visual Studio Code pada sistem operasi Windows <br/>
2. Upload video tutorial tersebut ke Youtube <br/>














