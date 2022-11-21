# Bab IV

## Tujuan Pembelajaran

* Mahasiswa dapat memahami konsep dasar dari bahasa Dart dan mengimplementasikannya dalam pembuatan aplikasi.


# Bahasa Pemrograman Dart

## Tentang Dart

Dart adalah bahasa pemrograman yang dikembangkan oleh Google, bersifat _object oriented_ dan bersifat _open source_. Bahasa pemrograman Dart  bersifat _strongly typed_ yang berarti setiap variabel harus memiliki tipe data. Akan tetapi Dart juga memiliki konsep _type inference_ yang berarti Dart akan menentukan tipe data dari variabel secara otomatis. Bahasa pemrograman Dart bisa di_compile_ menjadi kode JavaScript sehingga Dart bisa digunakan untuk membuat aplikasi web ataupun digunakan untuk membuat aplikasi _mobile_ dengan menggunakan framework Flutter.

Dart menyediakan _type safety_ yang berarti Dart akan mengecek apakah variabel yang digunakan sudah dideklarasikan atau belum. Dart juga menyediakan _runtime type checking_ yang berarti Dart akan mengecek apakah variabel yang digunakan sudah dideklarasikan atau belum. Selain itu, Dart juga menyediakan _Sound null safety_ yang berarti sebuah variabel tidak boleh berisi _null_ kecuali memang diperbolehkan. Dengan adanya _sound null safety_ maka akan mencegah _null exception_ saat _runtime_.

Berikut ini adalah contoh kode _Hello World_ pada Dart:

```dart
// Hello World
void main() {
  print('Hello World');
}
```

Keterangan:
  
    * ``// Hello World`` adalah komentar
    * `void` adalah tipe data yang digunakan untuk menandakan bahwa fungsi tersebut tidak mengembalikan nilai.
    * `main()` adalah fungsi yang akan dijalankan pertama kali saat program dijalankan.
    * `print()` adalah fungsi yang digunakan untuk mencetak teks ke layar.

## Variabel

### Deklarasi Variabel

Variabel adalah tempat untuk menyimpan data. Variabel pada Dart bersifat _strongly typed_ yang berarti setiap variabel harus memiliki tipe data. Akan tetapi Dart juga memiliki konsep _type inference_ yang berarti Dart akan menentukan tipe data dari variabel secara otomatis. Semua yang diletakkan di dalam variabel adalah _object_, dan setiap object adalah _instance_ dari sebuah _class_. Bahkan _number_, _function_ dan _null_ adalah _object_. 

Variabel pada Dart bersifat _case sensitive_ yang berarti penamaan variabel bersifat sensitif terhadap huruf besar dan huruf kecil. Untuk membuat sebuah variabel bisa berisi _null_ maka tanda tanya (?) harus ditambahkan setelah tipe data variabel. Contohnya, sebuah variabel bertipe data `String` bisa berisi _null_ dengan menambahkan tanda tanya (?) setelah tipe data `String` seperti `String?`.

Berikut ini adalah contoh kode untuk mendeklarasikan variabel pada Dart:

```dart
void main() {
  // Deklarasi variabel dengan tipe data
  String nama = 'Dart';
  int umur = 10;
  double tinggi = 1.5;
  bool isDart = true;

  // Deklarasi variabel tanpa tipe data dan type inference
  var nama = 'Dart';
  var umur = 10;
  var tinggi = 1.5;
  var isDart = true;
}
```

Pada kode tersebut terdapat 2 cara untuk mendeklarasikan variabel yaitu dengan menentukan tipe data dan tanpa menentukan tipe data. Jika kita mendeklarasikan variabel tanpa menentukan tipe data maka Dart akan menentukan tipe data dari variabel secara otomatis. Untuk mendeklarasikan variabel dengan tipe data maka kita harus menentukan tipe data dari variabel tersebut. Berikut ini adalah daftar tipe data yang tersedia pada Dart:

  * String
  * Numbers (int, double)
  * Boolean (bool)
  * List (Array)
  * Map
  * Runes
  * Symbols
  * Sets (Set)
  * Dynamic
  * nilai null (null)

Variabel yang belum diinisialisasi akan memiliki nilai _null_ secara otomatis. Bahkan variabel dengan tipe data numeric juga bisa berisi _null_ karena number (dan semua hal di Dart) adalah _object_.

### Tipe Data

Berikut ini adalah tipe data yang paling sering digunakan pada Dart:

#### Numbers

Tipe data `Numbers` pada Dart terdiri dari 2 jenis yaitu `int` dan `double`. Tipe data `int` digunakan untuk menyimpan bilangan bulat dan tipe data `double` digunakan untuk menyimpan bilangan pecahan. Berikut ini adalah contoh kode untuk mendeklarasikan variabel bertipe data `Numbers`:

```dart
void main() {
  // Deklarasi variabel bertipe data int
  int umur = 10;

  // Deklarasi variabel bertipe data double
  double tinggi = 1.5;
}
```

Selain `int` dan `double`, Dart juga menyediakan tipe data `num` yang merupakan _superclass_ dari `int` dan `double`. Tipe data `num` digunakan untuk menyimpan bilangan bulat dan pecahan. Berikut ini adalah contoh kode untuk mendeklarasikan variabel bertipe data `num`:

```dart
void main() {
  // Deklarasi variabel bertipe data num
  num umur = 10;
  num tinggi = 1.5;
}
```

#### String

Tipe data `String` digunakan untuk menyimpan teks (deretan unit kode UTF-16). Berikut ini adalah contoh kode untuk mendeklarasikan variabel bertipe data `String`:

```dart
void main() {
  // Deklarasi variabel bertipe data String
  String nama = 'Dart';
}
```

Single quote (') dan double quote (") dapat digunakan untuk mendeklarasikan variabel bertipe data `String`. Dalam string dapat dimasukkan ekpresi menggunakan `$` dan `{}`. Berikut ini adalah contoh kode untuk mendeklarasikan variabel bertipe data `String`:

```dart
void main() {
  // Deklarasi variabel bertipe data String
  print("Dart ${nama.toUpperCase()}"); // Dart DART
}
```

Untuk membuat string yang terdiri dari beberapa baris, kita bisa menggunakan triple quote ("""). Berikut ini adalah contoh kode untuk mendeklarasikan variabel bertipe data `String`:

```dart
void main() {
  // Deklarasi variabel bertipe data String
  String nama = '''
  Dart
  ''';
}
```

Sedangkan untuk membuat "raw" string, kita bisa menggunakan `r` sebelum string. Berikut ini adalah contoh kode untuk mendeklarasikan variabel bertipe data `String`:

```dart
void main() {
  // Deklarasi variabel bertipe data String
  String nama = r'Dart';
}
```

#### Boolean

Tipe data `Boolean` digunakan untuk menyimpan nilai `true` atau `false`. Berikut ini adalah contoh kode untuk mendeklarasikan variabel bertipe data `Boolean`:

```dart
void main() {
  // Deklarasi variabel bertipe data Boolean
  bool isDart = true;
}
```

#### List

Tipe data `List` digunakan untuk menyimpan kumpulan data. Tipe data `List` pada Dart merupakan _generic_ yang berarti kita harus menentukan tipe data dari data yang akan disimpan. Berikut ini adalah contoh kode untuk mendeklarasikan variabel bertipe data `List`:

```dart
void main() {
  // Deklarasi variabel bertipe data List
  List<String> nama = ['Dart', 'Flutter'];
}
```

List menggunakan indeks untuk mengakses data. Indeks dimulai dari 0 dan dapat diakses menggunakan `[]`. Untuk mendapatkan panjang dari list, kita bisa menggunakan `length`.

#### Map

Tipe data `Map` digunakan untuk menyimpan kumpulan data dengan pasangan key dan value. Berikut ini adalah contoh kode untuk mendeklarasikan variabel bertipe data `Map`:

```dart
void main() {
  // Deklarasi variabel bertipe data Map
  Map<String, String> nama = {
    'namaDepan': 'Dart',
    'namaBelakang': 'Flutter'
  };

  // Mengakses value dari key
  print(nama['namaDepan']); // Dart

  var nama = Map<String, String>();
  nama['namaDepan'] = 'Dart';
  nama['namaBelakang'] = 'Flutter';
}
```

Map menggunakan key untuk mengakses data. Untuk mendapatkan panjang dari map, kita bisa menggunakan `length`. Jika key tidak ditemukan, maka akan mengembalikan nilai _null_.

#### Dynamic
Selain tipe data yang sudah disebutkan sebelumnya, Dart juga menyediakan tipe `Dynamic`. Tipe data `Dynamic` digunakan untuk menyimpan data dengan tipe data yang berbeda-beda. Berikut ini adalah contoh kode untuk mendeklarasikan variabel bertipe data `Dynamic`:

```dart
void main() {
  // Deklarasi variabel bertipe data Dynamic
  dynamic nama = 'Dart';
  nama = 10;
  nama = true;
}
```

### Final dan Const

Jika kita ingin membuat sebuah variabel yang nilainya tidak bisa diubah lagi maka kita bisa menggunakan kata kunci `final` atau `const` daripada menggunakan `var`. Variabel yang final hanya dapat diset sekali saja, dan setelah itu nilainya tidak bisa diubah lagi. Sedangkan variabel yang const harus diinisialisasi saat deklarasi dan nilainya tidak bisa diubah lagi. 

```dart
void main() {
  // Deklarasi variabel final
  final nama = 'Budi Santoso';
  final String namaSingkat = 'Budi';

  // Deklarasi variabel const
  const umur = 10;
  const int umur = 10;
}
```

## Operator

Sama dengan bahasa pemrograman lain, Dart juga memiliki operator untuk melakukan operasi matematika, perbandingan, logika, bitwise, dan lain-lain. Berikut ini adalah daftar operator yang tersedia pada Dart:

  * Aritmatika
  * Perbandingan
  * Logika
  * Bitwise
  * Ternary
  * Assignment
  * Type test
  * Type cast
  * Cascade notation

### Aritmatika

Operator aritmatika digunakan untuk melakukan operasi matematika seperti penjumlahan, pengurangan, perkalian, pembagian, dan lain-lain. Berikut ini adalah daftar operator aritmatika yang tersedia pada Dart:

  * `+` : Penjumlahan
  * `-` : Pengurangan
  * `*` : Perkalian
  * `/` : Pembagian
  * `%` : Modulus
  * `~/` : Pembagian dengan pembulatan ke bawah

### Perbandingan

Operator perbandingan digunakan untuk membandingkan dua buah nilai. Berikut ini adalah daftar operator perbandingan yang tersedia pada Dart:

  * `==` : Sama dengan
  * `!=` : Tidak sama dengan
  * `>` : Lebih besar dari
  * `<` : Lebih kecil dari
  * `>=` : Lebih besar dari atau sama dengan
  * `<=` : Lebih kecil dari atau sama dengan

### Logika

Operator logika digunakan untuk menggabungkan dua buah kondisi. Berikut ini adalah daftar operator logika yang tersedia pada Dart:

  * `&&` : Dan
  * `||` : Atau
  * `!` : Negasi

### Bitwise

Operator bitwise digunakan untuk melakukan operasi pada bit. Berikut ini adalah daftar operator bitwise yang tersedia pada Dart:

  * `&` : AND
  * `|` : OR
  * `^` : XOR
  * `~` : NOT
  * `<<` : Shift left
  * `>>` : Shift right

### Ternary

Operator terna digunakan untuk mengeksekusi dua buah ekspresi berdasarkan kondisi. Berikut ini adalah contoh kode untuk menggunakan operator ternary:

```dart
void main() {
  // Deklarasi variabel
  int a = 10;
  int b = 20;

  // Menggunakan operator ternary
  int c = a > b ? a : b;
  print(c); // 20
}
```

Pada kode diatas, variabel `c` akan bernilai sama dengan variabel `b` karena kondisi `a > b` bernilai _false_ dikarenakan `a` lebih kecil dari `b`.

### Assignment

Operator assignment digunakan untuk mengisi nilai ke dalam variabel. Berikut ini adalah daftar operator assignment yang tersedia pada Dart:

  * `=` : Assignment
  * `+=` : Penjumlahan assignment
  * `-=` : Pengurangan assignment
  * `*=` : Perkalian assignment
  * `/=` : Pembagian assignment
  * `%=` : Modulus assignment
  * `~/=` : Pembagian dengan pembulatan ke bawah assignment
  * `&=` : AND assignment
  * `|=` : OR assignment
  * `^=` : XOR assignment
  * `<<=` : Shift left assignment
  * `>>=` : Shift right assignment

## Control Flow (Struktur Kendali)

Struktur kendali digunakan untuk mengontrol jalannya program. Struktur kendali yang dimiliki oleh Dart sama sepert bahasa pemrograman lain seperti Java, C++ dan lainnya. Pada Dart, terdapat beberapa struktur kendali yang bisa digunakan, yaitu:

  * If
  * If-else
  * If-else-if
  * Switch
  * For
  * For-in
  * While
  * Do-while
  * Break
  * Continue

### If

Struktur kendali if digunakan untuk mengeksekusi kode jika kondisi bernilai _true_. Berikut ini adalah contoh kode untuk menggunakan struktur kendali if:

```dart
void main() {
  // Deklarasi variabel
  int a = 10;
  int b = 20;

  // Menggunakan struktur kendali if
  if (a > b) {
    print('a lebih besar dari b');
  }
}
```

Pada kode diatas, karena kondisi `a > b` bernilai _false_ maka kode yang ada di dalam blok if tidak akan dieksekusi.

### If-else

Struktur kendali if-else digunakan untuk mengeksekusi kode jika kondisi bernilai _true_ dan mengeksekusi kode lain jika kondisi bernilai _false_. Berikut ini adalah contoh kode untuk menggunakan struktur kendali if-else:

```dart
void main() {
  // Deklarasi variabel
  int a = 10;
  int b = 20;

  // Menggunakan struktur kendali if-else
  if (a > b) {
    print('a lebih besar dari b');
  } else {
    print('a lebih kecil dari b');
  }
}
```

Pada kode diatas, karena kondisi `a > b` bernilai _false_ maka kode yang ada di dalam blok if tidak akan dieksekusi, namun kode yang ada di dalam blok else akan dieksekusi.

### If-else-if

Struktur kendali if-else-if digunakan untuk mengeksekusi kode jika kondisi bernilai _true_ dan mengeksekusi kode lain jika kondisi bernilai _false_. Berikut ini adalah contoh kode untuk menggunakan struktur kendali if-else-if:

```dart
void main() {
  // Deklarasi variabel
  int a = 10;
  int b = 20;
  int c = 30;

  // Menggunakan struktur kendali if-else-if
  if (a > b) {
    print('a lebih besar dari b');
  } else if (a > c) {
    print('a lebih besar dari c');
  } else {
    print('a lebih kecil dari b dan c');
  }
}
```

Pada kode diatas, karena kondisi `a > b` bernilai _false_ maka kode yang ada di dalam blok if tidak akan dieksekusi, namun karena kondisi `a > c` bernilai _false_ maka kode yang ada di dalam blok else-if juga tidak akan dieksekusi, dan kode yang ada di dalam blok else akan dieksekusi.

### Switch

Struktur kendali switch digunakan untuk mengeksekusi kode berdasarkan nilai dari variabel. Berikut ini adalah contoh kode untuk menggunakan struktur kendali switch:

```dart
void main() {
  // Deklarasi variabel
  int a = 10;

  // Menggunakan struktur kendali switch
  switch (a) {
    case 10:
      print('a bernilai 10');
      break;
    case 20:
      print('a bernilai 20');
      break;
    default:
      print('a tidak bernilai 10 dan 20');
  }
}
```

Pada kode diatas, karena nilai dari variabel `a` adalah 10 maka kode yang ada di dalam blok case 10 akan dieksekusi.

### For

Struktur kendali for digunakan untuk mengeksekusi kode berulang kali. Berikut ini adalah contoh kode untuk menggunakan struktur kendali for:

```dart
void main() {
  // Menggunakan struktur kendali for
  for (int i = 0; i < 10; i++) {
    print('Perulangan ke-$i');
  }
}
```

Pada kode diatas, kode yang ada di dalam blok for akan dieksekusi sebanyak 10 kali.

### For-in

Struktur kendali for-in digunakan untuk mengeksekusi kode berulang kali untuk setiap item di dalam list. Berikut ini adalah contoh kode untuk menggunakan struktur kendali for-in:

```dart
void main() {
  // Deklarasi list
  List<int> list = [1, 2, 3, 4, 5];

  // Menggunakan struktur kendali for-in
  for (int i in list) {
    print('Perulangan ke-$i');
  }
}
```

Pada kode diatas, kode yang ada di dalam blok for-in akan dieksekusi sebanyak 5 kali.

### While

Struktur kendali while digunakan untuk mengeksekusi kode berulang kali selama kondisi bernilai _true_. Berikut ini adalah contoh kode untuk menggunakan struktur kendali while:

```dart
void main() {
  // Deklarasi variabel
  int i = 0;

  // Menggunakan struktur kendali while
  while (i < 10) {
    print('Perulangan ke-$i');
    i++;
  }
}
```

Pada kode diatas, kode yang ada di dalam blok while akan dieksekusi sebanyak 10 kali.

### Do-while

Struktur kendali do-while digunakan untuk mengeksekusi kode berulang kali selama kondisi bernilai _true_. Berikut ini adalah contoh kode untuk menggunakan struktur kendali do-while:

```dart
void main() {
  // Deklarasi variabel
  int i = 0;

  // Menggunakan struktur kendali do-while
  do {
    print('Perulangan ke-$i');
    i++;
  } while (i < 10);
}
```

Pada kode diatas, kode yang ada di dalam blok do-while akan dieksekusi sebanyak 10 kali.

## Fungsi

Fungsi adalah blok kode yang digunakan untuk melakukan suatu tugas tertentu. Fungsi dapat dipanggil kapan saja dan berapa kali yang diperlukan. Fungsi dapat menerima parameter dan mengembalikan nilai. Berikut ini adalah contoh kode untuk membuat fungsi:

```dart
// Fungsi tanpa parameter dan tanpa nilai kembalian
void main() {
  print('Hello World');
}
```

Beberapa fungsi yang sering digunakan diantaranya adalah:

  * `print()` digunakan untuk mencetak teks ke layar.
  * `int.parse()` digunakan untuk mengubah tipe data String ke tipe data int.
  * `double.parse()` digunakan untuk mengubah tipe data String ke tipe data double.
  * `toString()` digunakan untuk mengubah tipe data int atau double ke tipe data String.

## Class

Untuk dapat menggunakan bahasa pemrograman Dart dengan baik, kita harus memahami konsep _class_. _Class_ merupakan sebuah _blueprint_ atau _template_ yang digunakan untuk membuat sebuah _object_. _Class_ dapat diartikan sebagai sebuah _custom data type_ yang dapat kita buat sendiri. Sebuah _class_ dapat memiliki _properties_ dan _methods_. _Properties_ adalah variabel yang ada di dalam sebuah _class_, sedangkan _methods_ adalah fungsi yang ada di dalam sebuah _class_.

### Membuat Class

Untuk membuat sebuah _class_, kita bisa menggunakan kata kunci `class` dan nama _class_ yang diikuti dengan kurung kurawal `{}`. Berikut ini adalah contoh kode untuk membuat _class_:

```dart
class Person {
  String nama;
  int umur;
}
```

### Membuat Object

Setelah kita membuat _class_, kita bisa membuat _object_ dari _class_ tersebut. Berbeda dengan bahasa pemrograman lain yang menggunakan kata kunci `new`, untuk membuat _object_ dari _class_ di Dart kita bisa menggunakan nama _class_ yang diikuti dengan kurung kurawal `()` tanpa diawali dengan kata kunci `new`. Berikut ini adalah contoh kode untuk membuat _object_ dari _class_ `Person`:

```dart
void main() {
  // Membuat object dari class Person
  Person person = Person();
}
```

### Constructor

Constructor adalah sebuah fungsi yang akan dipanggil saat kita membuat _object_ dari sebuah _class_. Constructor digunakan untuk menginisialisasi nilai awal dari sebuah _object_. Constructor memiliki nama yang sama dengan nama _class_ dan tidak memiliki tipe data kembalian. Berikut ini adalah contoh kode untuk membuat _constructor_:

```dart
class Person {
  String nama;
  int umur;

  // Constructor
  Person(String nama, int umur) {
    this.nama = nama;
    this.umur = umur;
  }
}
```

Constructor ditandai dengan nama yang sama dengan nama _class_ dan tidak memiliki tipe data kembalian. Kata kunci `this` untuk mengakses variabel _instance_ dari _class_.

### Encapsulation

Encapsulation adalah salah satu konsep dalam OOP yang digunakan untuk menyembunyikan detail dari sebuah _object_ dari _object_ lain. Encapsulation dapat dicapai dengan cara membuat variabel _instance_ dari _class_ menjadi private. Di Dart, variabel _instance_ dari _class_ dapat dijadikan private dengan cara menambahkan underscore `_` di depan nama variabel. Berikut ini adalah contoh kode untuk membuat variabel _instance_ menjadi private:

```dart
class Person {
  String _nama;
  int _umur;
}
```

Pada kode di atas, variabel `_nama` dan `_umur` menjadi private. Untuk mengakses variabel private tersebut, kita bisa menggunakan getter dan setter. Berikut ini adalah contoh kode untuk membuat getter dan setter:

```dart
class Person {
  String _nama;
  int _umur;

  // Getter
  String get nama => _nama;

  // Setter
  set nama(String value) {
    _nama = value;
  }
}
```

## Pemrograman Asynchronous

Pemrograman asynchronous adalah sebuah teknik yang digunakan untuk melakukan eksekusi kode secara bersamaan. Pemrograman asynchronous dapat digunakan untuk mengurangi _blocking_ pada aplikasi. Pemrograman asynchronous di Dart menggunakan konsep _Future_ dan _Stream_. _Future_ digunakan untuk melakukan eksekusi kode secara asynchronous dan mengembalikan nilai. _Stream_ digunakan untuk melakukan eksekusi kode secara asynchronous dan mengembalikan banyak nilai.

### Future

_Future_ adalah sebuah _promise_ yang akan mengembalikan nilai di masa yang akan datang. _Future_ digunakan untuk melakukan eksekusi kode secara asynchronous dan mengembalikan nilai. Berikut ini adalah contoh kode untuk menggunakan _Future_:

```dart
void main() {
  // Membuat Future
  Future<String> future = Future.delayed(Duration(seconds: 2), () {
    return 'Hello World';
  });

  // Menggunakan Future
  future.then((value) => print(value));
}
```

Pada kode di atas, kita membuat sebuah _Future_ dengan menggunakan kata kunci `Future` dan nama _Future_ yang diikuti dengan kurung kurawal `()`. _Future_ tersebut akan mengembalikan nilai `Hello World` setelah 2 detik. Setelah itu, kita menggunakan _Future_ tersebut dengan menggunakan kata kunci `then` dan nama _Future_ yang diikuti dengan kurung kurawal `()`. Pada kurung kurawal tersebut, kita bisa menambahkan fungsi yang akan dieksekusi ketika _Future_ tersebut selesai.

Sebuah _promise_ yang akan mengembalikan nilai di masa yang akan datang terdiri dari 3 bagian, yaitu:

  * _Future_ yang akan mengembalikan nilai di masa yang akan datang.
  * _then_ yang akan dieksekusi ketika _Future_ selesai.
  * _catchError_ yang akan dieksekusi ketika terjadi error.

Berikut ini adalah contoh kode untuk menggunakan _promise_:
  
```dart
void main() {
  // Membuat Future
  Future<String> future = Future.delayed(Duration(seconds: 2), () {
    return 'Hello World';
  });

  // Menggunakan Future
  future
    .then((value) => print(value))
    .catchError((error) => print(error));
}
```

#### Async dan Await

Async dan await adalah sebuah kata kunci yang digunakan untuk melakukan eksekusi kode secara asynchronous. Async digunakan untuk membuat sebuah fungsi menjadi asynchronous. Await digunakan untuk menunggu sebuah _Future_ selesai. Berikut ini adalah contoh kode untuk menggunakan async dan await:

```dart
void main() async {
  // Membuat Future
  Future<String> future = Future.delayed(Duration(seconds: 2), () {
    return 'Hello World';
  });

  // Menggunakan Future
  String result = await future;
  print(result);
}
```

Pada kode di atas, kita membuat sebuah fungsi `main` menjadi asynchronous dengan menggunakan kata kunci `async`. Setelah itu, kita membuat sebuah _Future_ yang akan mengembalikan nilai `Hello World` setelah 2 detik. Kita menggunakan _Future_ tersebut dengan menggunakan kata kunci `await` di depan nama _Future_ yang akan menunggu _Future_ tersebut selesai. Setelah _Future_ tersebut selesai, kita bisa mengakses nilai yang dikembalikan oleh _Future_ tersebut. Pada kode di atas, kita mengakses nilai yang dikembalikan oleh _Future_ tersebut dengan menggunakan variabel `result`.

#### Menangani Error

Untuk menangani error dalam fungsi `async`, digunakan `try-catch`. Berikut ini adalah contoh kode untuk menangani error:

```dart
void main() async {
  try {
    // Membuat Future
    Future<String> future = Future.delayed(Duration(seconds: 2), () {
      return 'Hello World';
    });

    // Menggunakan Future
    String result = await future;
    print(result);
  } catch (error) {
    print(error);
  }
}
```



### Stream

_Stream_ adalah sebuah _promise_ yang akan mengembalikan banyak nilai di masa yang akan datang. _Stream_ digunakan untuk melakukan eksekusi kode secara asynchronous dan mengembalikan banyak nilai. Berikut ini adalah contoh kode untuk menggunakan _Stream_:

```dart
void main() {
  // Membuat Stream
  Stream<int> stream = Stream.periodic(Duration(seconds: 1), (int value) {
    return value;
  });

  // Menggunakan Stream
  stream.take(5).listen((value) => print(value));
}
```

Pada kode di atas, kita membuat sebuah _Stream_ dengan menggunakan kata kunci `Stream` dan nama _Stream_ yang diikuti dengan kurung kurawal `()`. _Stream_ tersebut akan mengembalikan nilai `0` setiap 1 detik. Setelah itu, kita menggunakan _Stream_ tersebut dengan menggunakan kata kunci `listen` dan nama _Stream_ yang diikuti dengan kurung kurawal `()`. Pada kurung kurawal tersebut, kita bisa menambahkan fungsi yang akan dieksekusi ketika _Stream_ tersebut mengembalikan nilai.

#### Operasi Stream

Class `Stream` memiliki beberapa method yang digunakan untuk melakukan operasi pada _Stream_.

  * `map` digunakan untuk mengubah nilai yang dikembalikan oleh _Stream_.
  * `where` digunakan untuk memfilter nilai yang dikembalikan oleh _Stream_.
  * `take` digunakan untuk mengambil nilai yang dikembalikan oleh _Stream_.
  * `listen` digunakan untuk menangani nilai yang dikembalikan oleh _Stream_.
  * `transform` digunakan untuk melakukan operasi pada nilai yang dikembalikan oleh _Stream_.

## Pustaka di Dart

### Pustaka Dart

Pustaka Dart adalah sebuah pustaka yang sudah disediakan oleh Dart. Pustaka Dart sudah disediakan secara default ketika kita membuat sebuah proyek baru. Berikut ini adalah beberapa pustaka Dart yang sering digunakan:

  * `dart:core` adalah pustaka yang berisi fungsi-fungsi dasar dari Dart.
  * `dart:async` adalah pustaka yang berisi fungsi-fungsi untuk melakukan eksekusi kode secara asynchronous.
  * `dart:math` adalah pustaka yang berisi fungsi-fungsi untuk melakukan operasi matematika.
  * `dart:io` adalah pustaka yang berisi fungsi-fungsi untuk melakukan operasi input dan output.
  * `dart:convert` adalah pustaka yang berisi fungsi-fungsi untuk melakukan konversi tipe data.

### Pustaka Eksternal

Selain pustaka Dart, kita juga bisa menggunakan pustaka eksternal. Pustaka eksternal adalah pustaka yang dibuat oleh orang lain. Pustaka eksternal bisa kita gunakan untuk mempermudah kita dalam membuat aplikasi. Pustaka eksternal Dart berada di [pub.dev](https://pub.dev/). Berikut ini adalah beberapa pustaka eksternal yang sering digunakan:

  * `http` adalah pustaka yang digunakan untuk melakukan request ke server.
  * `shared_preferences` adalah pustaka yang digunakan untuk menyimpan data secara lokal.
  * `flutter_bloc` adalah pustaka yang digunakan untuk membuat aplikasi dengan arsitektur BLoC.
  * `flutter_svg` adalah pustaka yang digunakan untuk menampilkan SVG di Flutter.

## Penggunaan Pustaka

### Penggunaan Pustaka Dart

Untuk menggunakan pustaka Dart, kita bisa menggunakan kata kunci `import` di awal kode. Berikut ini adalah contoh kode untuk menggunakan pustaka `dart:math`:

```dart
import 'dart:math';
```

### Penggunaan Pustaka Eksternal

Untuk menggunakan pustaka eksternal, kita bisa menggunakan kata kunci `import` di awal kode. Berikut ini adalah contoh kode untuk menggunakan pustaka `http`:

```dart
import 'package:http/http.dart' as http;
```

## Platform Dart

### Platform Dart

Platform Dart adalah sebuah platform yang digunakan untuk menjalankan kode Dart. Platform Dart bisa berupa aplikasi, web, dan lain-lain. Berikut ini adalah beberapa platform Dart yang sering digunakan:

  * `Dart VM` adalah platform Dart yang digunakan untuk menjalankan kode Dart di terminal.
  * `Flutter` adalah platform Dart yang digunakan untuk membuat aplikasi mobile.
  * `DartPad` adalah platform Dart yang digunakan untuk menjalankan kode Dart di browser.
  * `Dart DevTools` adalah platform Dart yang digunakan untuk melakukan debugging pada aplikasi Flutter.


## Referensi

  1. [Dart Programming Language](https://dart.dev/)
  2. [Dart Programming Language - Getting Started](https://dart.dev/get-dart)
  3. [Dart Programming Language - Language Tour](https://dart.dev/guides/language/language-tour)
  4. [Dart Programming Language - Language Tour - Variables](https://dart.dev/guides/language/language-tour#variables)
  5. [Dart Programming Language - Language Tour - Built-in Types](https://dart.dev/guides/language/language-tour#built-in-types)
  6. [Dart Programming Language - Language Tour - Functions](https://dart.dev/guides/language/language-tour#functions)
  7. [Dart Programming Language - Language Tour - Asynchrony Support](https://dart.dev/guides/language/language-tour#asynchrony-support)
  8. [Dart Programming Language - Language Tour - Libraries and Visibility](https://dart.dev/guides/language/language-tour#libraries-and-visibility)
  9. [Dart Programming Language - Language Tour - Exceptions](https://dart.dev/guides/language/language-tour#exceptions)
  10. [Dart Programming Language - Language Tour - Generics](https://dart.dev/guides/language/language-tour#generics)
  11. [Dart Programming Language - Language Tour - Typedefs](https://dart.dev/guides/language/language-tour#typedefs)
  12. [Dart Programming Language - Language Tour - Metadata](https://dart.dev/guides/language/language-tour#metadata)
  13. [Dart Programming Language - Language Tour - Comments](https://dart.dev/guides/language/language-tour#comments)
  14. [Dart Programming Language - Language Tour - Keywords](https://dart.dev/guides/language/language-tour#keywords)
  15. [Dart Programming Language - Language Tour - Libraries and Scripts](https://dart.dev/guides/language/language-tour#libraries-and-scripts)
  16. [Dart Programming Language - Language Tour - Dart Packages](https://dart.dev/guides/language/language-tour#dart-packages)
  17. [Dart Programming Language - Language Tour - Dart Libraries](https://dart.dev/guides/language/language-tour#dart-libraries)

## Kesimpulan

Dart adalah bahasa pemrograman yang dikembangkan oleh Google. Dart memiliki banyak fitur yang memudahkan kita dalam membuat aplikasi. Dart memiliki banyak pustaka yang bisa kita gunakan untuk mempermudah kita dalam membuat aplikasi. Dart juga memiliki banyak platform yang bisa kita gunakan untuk menjalankan kode Dart.

## Tugas

1. Buatlah aplikasi sederhana dengan menggunakan bahasa pemrograman Dart.
2. Buatlah aplikasi sederhana dengan menggunakan bahasa pemrograman Dart yang menggunakan pustaka `http` untuk melakukan request ke server.
