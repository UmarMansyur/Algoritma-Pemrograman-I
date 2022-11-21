# Bab V

## Tujuan Pembelajaran

* Mahasiswa dapat memahami konsep dasar dari Flutter dan Dart serta dapat mengimplementasikannya dalam pembuatan aplikasi mobile.

## Flutter

## Tentang Flutter

Flutter adalah framework open source yang dibuat oleh Google untuk membangun aplikasi mobile cross-platform. Flutter menggunakan bahasa Dart sebagai bahasa utamanya. Flutter dapat digunakan untuk membuat aplikasi Android dan iOS. Flutter menggunakan teknologi yang sama untuk membuat aplikasi Android dan iOS, sehingga memungkinkan developer untuk membuat aplikasi yang dapat berjalan di dua platform tersebut dengan menggunakan satu kode basis. Selain itu, Flutter juga dapat digunakan untuk membuat aplikasi desktop dan web. 

## Kelebihan Flutter

* Flutter menggunakan bahasa Dart sebagai bahasa utamanya. Dart adalah bahasa yang mudah dipelajari dan memiliki sintaks yang mirip dengan bahasa pemrograman yang sudah ada seperti Java, C#, JavaScript, dan lain-lain.

* Flutter menggunakan widget sebagai komponen utama dalam pembuatan aplikasi. Widget adalah komponen yang dapat digunakan untuk membuat tampilan aplikasi. Widget dapat digunakan untuk membuat tampilan aplikasi yang berbeda-beda. Widget akan mempermudah developer dalam membuat aplikasi karena developer tidak perlu membuat tampilan dari awal.

* Flutter menggunakan konsep hot reload. Hot reload adalah konsep yang memungkinkan developer untuk melihat perubahan yang terjadi pada aplikasi tanpa harus melakukan proses build ulang. Hal ini memungkinkan developer untuk melihat perubahan yang terjadi pada aplikasi secara langsung sehingga memudahkan developer untuk melakukan debugging dan mempercepat proses pengembangan aplikasi.

* Flutter menggunakan konsep material design. Material design adalah implementasi dari konsep material design yang digunakan oleh Google untuk membuat aplikasi Android. Sedangkan, Untuk pengembangan di lingkungan iOS,  Flutter menggunakan konsep Cupertino design. Cupertino design adalah implementasi dari konsep material design yang digunakan oleh Apple untuk membuat aplikasi iOS.

* Flutter menggunakan konsep native code. Native code adalah konsep yang memungkinkan developer untuk membuat aplikasi yang dapat berjalan pada platform tertentu menggunakan bahasa pemrograman yang digunakan pada platform tersebut.

* Flutter menggunakan konsep stateless dan stateful widget. Stateless widget adalah widget yang tidak memiliki state. Stateless widget hanya dapat digunakan untuk membuat tampilan aplikasi yang statis. Stateful widget adalah widget yang memiliki state.

* Flutter menggunakan konsep widget tree. Dengan menggunakan widget tree, developer dapat membuat tampilan aplikasi yang kompleks dengan mudah.


## Membuat Aplikasi Flutter Pertama

Untuk membuat aplikasi Flutter pertama, kita perlu menginstall Flutter SDK terlebih dahulu. Untuk menginstall Flutter SDK, kita dapat mengikuti langkah-langkah yang tertera pada [https://flutter.dev/docs/get-started/install](https://flutter.dev/docs/get-started/install) berikut.

Setelah menginstall Flutter SDK, kita dapat membuat aplikasi Flutter pertama kita dengan menjalankan perintah berikut pada terminal.

```bash
flutter create myapp
```

Perintah di atas akan membuat folder bernama myapp yang berisi kode basis aplikasi Flutter pertama kita. Untuk menjalankan aplikasi Flutter pertama kita, kita dapat menjalankan perintah berikut pada terminal.

```bash
cd myapp
flutter run
```

## Widget

Widget dalam Flutter dibangun menggunakan framework modern yang fleksibel dan reactive. Widget menggambarkan seperti apa tampilan yang akan ditampilkan pada layar berdasarkan konfigurasi dan state saat ini. Ketika state berubah, widget akan meminta framework untuk membangun ulang tampilan yang sesuai dengan state baru. Widget dapat berupa stateless atau stateful. Widget stateless tidak memiliki state sedangkan widget stateful memiliki state.

Untuk membuat aplikasi sederhana dengan Flutter, dapat dilihat pada contoh berikut:

```dart
import 'package:flutter/material.dart';

void main() {
  runApp(
    MaterialApp(
      home: Scaffold(
        appBar: AppBar(
          title: Text('Hello World'),
        ),
        body: Center(
          child: Text('Hello World'),
        ),
      ),
    ),
  );
}
```

Pada contoh di atas, fungsi `runApp()` menggunakan widget `MaterialApp` sebagai widget utama. Widget `MaterialApp` merupakan widget yang digunakan untuk membuat aplikasi yang menggunakan konsep material design. Widget `MaterialApp` memiliki properti `home` yang digunakan untuk menentukan widget apa yang akan ditampilkan pada layar. Pada contoh di atas, widget `Scaffold` digunakan sebagai widget yang akan ditampilkan pada layar. Widget `Scaffold` merupakan widget yang digunakan untuk membuat tampilan aplikasi yang menggunakan konsep material design. 

Widget `Scaffold` memiliki properti `appBar` yang digunakan untuk menentukan widget apa yang akan ditampilkan pada bagian atas aplikasi. Pada contoh di atas, widget `AppBar` digunakan sebagai widget yang akan ditampilkan pada bagian atas aplikasi. Widget `AppBar` memiliki properti `title` yang digunakan untuk menentukan widget apa yang akan ditampilkan pada bagian tengah dari widget `AppBar`. Pada contoh di atas, widget `Text` digunakan sebagai widget yang akan ditampilkan pada bagian tengah dari widget `AppBar`. Widget `Text` memiliki properti `child` yang digunakan untuk menentukan teks apa yang akan ditampilkan pada widget `Text`. Pada contoh di atas, widget `Text` akan menampilkan teks `Hello World` pada widget `Text`.

## Stateful Widget

Flutter memiliki dua jenis widget, yaitu stateless widget dan stateful widget. Stateless widget adalah widget yang tidak memiliki state. Stateless widget hanya dapat digunakan untuk membuat tampilan aplikasi yang statis. Stateful widget adalah widget yang memiliki state. Stateful widget dapat digunakan untuk membuat tampilan aplikasi yang dinamis.

Stateful widget adalah widget yang dinamis: contohnya, dia dapat mengubah tampilannya sebagai respons terhadap interaksi pengguna atau perubahan data. Untuk membuat stateful widget, kita perlu mengimplementasikan dua kelas: StatefulWidget dan State. Kita akan mengganti contoh stateless widget sebelumnya dengan stateful widget yang mengelola interaksi pengguna.

```dart
import 'package:flutter/material.dart';

void main() {
  runApp(MyApp());
}

class MyApp extends StatefulWidget {
  @override
  _MyAppState createState() => _MyAppState();
}

class _MyAppState extends State<MyApp> {
  int counter = 0;

  @override
  Widget build(BuildContext context) {
    return MaterialApp(
      home: Scaffold(
        appBar: AppBar(
          title: Text('Stateful Widget'),
        ),
        body: Center(
          child: Text('Counter: $counter'),
        ),
        floatingActionButton: FloatingActionButton(
          child: Icon(Icons.add),
          onPressed: () {
            setState(() {
              counter++;
            });
          },
        ),
      ),
    );
  }
}
```

Stateful widget memiliki dua kelas, yaitu StatefulWidget dan State. Kita membuat stateful widget yang memiliki state yang bertipe integer. Stateful widget memiliki properti `counter` yang digunakan untuk menyimpan nilai integer. Pada contoh di atas, nilai integer yang disimpan pada properti `counter` adalah 0. 

Ketika kita menekan tombol tambah, maka nilai integer pada properti `counter` akan bertambah 1. Pada contoh di atas, nilai integer pada properti `counter` akan bertambah 1 ketika kita menekan tombol tambah. Ketika kita menekan tombol tambah, maka fungsi `setState()` akan dipanggil. Fungsi `setState()` akan memanggil fungsi `build()` kembali untuk membuat ulang tampilan aplikasi. Pada contoh di atas, fungsi `build()` akan membuat ulang tampilan aplikasi dengan menampilkan nilai integer yang disimpan pada properti `counter`.

## State Management

Terdapat beberapa cara untuk mengelola state pada aplikasi Flutter yaitu:

  * Widget mengatur sendiri state-nya
  * Widget menggunakan parent untuk mengatur state-nya
  * Menggunakan state management package (provider, bloc, redux, dll)

### Widget State

Widget state adalah cara yang paling sederhana untuk mengelola state pada aplikasi Flutter. Widget state digunakan untuk mengelola state pada widget yang memiliki state. Widget state dapat digunakan untuk membuat aplikasi yang sederhana. Namun, widget state tidak dapat digunakan untuk membuat aplikasi yang kompleks.

### Parent State

Seringkali kita ingin membuat aplikasi yang kompleks dengan menggunakan widget state. Namun, widget state tidak dapat digunakan untuk membuat aplikasi yang kompleks. Untuk membuat aplikasi yang kompleks, kita dapat menggunakan parent state. Tampilan widget ditentukan oleh state yang disimpan pada parent widget. Parent widget akan mengirimkan state ke child widget melalui properti. Ketika state pada parent widget berubah, maka child widget akan membuat ulang tampilan widgetnya.

### State Management Package

Untuk aplikasi yang kompleks dan terdiri dari banyak widget, kita dapat menggunakan state management package. Salah satu state management package yang dapat digunakan pada aplikasi Flutter adalah provider. Peran dari provider adalah untuk menyediakan state yang dapat digunakan oleh widget tanpa harus mengirimkan state melalui properti. Provider akan mengirimkan state ke widget yang membutuhkan state tersebut. Ketika state pada provider berubah, maka widget yang menggunakan state tersebut akan membuat ulang tampilan widgetnya.

Untuk dapat menggunakan provider, kita perlu menambahkan dependency pada pubspec.yaml.

```yaml
dependencies:
  flutter:
    sdk: flutter
  provider: ^6.0.0
```

Kemudian, kita perlu mengimport package provider.

```dart
import 'package:provider/provider.dart';
```

Dalam penggunaan `provider`, kita harus memahami tiga konsep yaitu:

  * ChangeNotifier
  * ChangeNotifierProvider
  * Consumer

#### ChangeNotifier

ChangeNotifier adalah class sederhana yang dapat digunakan untuk mengenkapsulasi state. Untuk aplikasi yang sederhana, kita dapat menggunakan satu ChangeNotifier. Namun, untuk aplikasi yang kompleks, kita dapat menggunakan banyak ChangeNotifier untuk mengelola state.

Berikut adalah contoh penggunaan ChangeNotifier.

```dart
class Counter extends ChangeNotifier {
  int _counter = 0;

  int get counter => _counter;

  void increment() {
    _counter++;
    notifyListeners();
  }
}
```

Pada contoh di atas, kita membuat class Counter yang mengimplementasikan ChangeNotifier. Class Counter memiliki properti `_counter` yang digunakan untuk menyimpan nilai integer. Pada contoh di atas, nilai integer yang disimpan pada properti `_counter` adalah 0. Class Counter memiliki getter `counter` yang digunakan untuk mengambil nilai integer yang disimpan pada properti `_counter`. Class Counter memiliki fungsi `increment()` yang digunakan untuk menambahkan nilai integer pada properti `_counter`. Fungsi `increment()` akan memanggil fungsi `notifyListeners()` untuk memberitahu widget yang menggunakan state tersebut untuk membuat ulang tampilan widgetnya.

#### ChangeNotifierProvider

ChangeNotifierProvider digunakan untuk menyediakan state yang dapat digunakan oleh widget tanpa harus mengirimkan state melalui properti. ChangeNotifierProvider akan mengirimkan state ke widget yang membutuhkan state tersebut. Ketika state pada ChangeNotifierProvider berubah, maka widget yang menggunakan state tersebut akan membuat ulang tampilan widgetnya.

ChangeNotifierProvider diletakkan diatas widget-widget yang membutuhkan state. Berikut adalah contoh penggunaan ChangeNotifierProvider.

```dart
class MyApp extends StatelessWidget {
  @override
  Widget build(BuildContext context) {
    return ChangeNotifierProvider(
      create: (context) => Counter(),
      child: MaterialApp(
        home: HomePage(),
      ),
    );
  }
}
```

Jika membutuhkan lebih dari satu ChangeNotifier, maka ChangeNotifierProvider dapat digunakan untuk menyediakan banyak ChangeNotifier.

```dart
class MyApp extends StatelessWidget {
  @override
  Widget build(BuildContext context) {
    return MultiProvider(
      providers: [
        ChangeNotifierProvider(create: (context) => Counter()),
        ChangeNotifierProvider(create: (context) => Counter2()),
      ],
      child: MaterialApp(
        home: HomePage(),
      ),
    );
  }
}
```

#### Consumer

Consumer digunakan untuk mengambil state yang disediakan oleh ChangeNotifierProvider. Consumer akan membuat ulang tampilan widgetnya ketika state pada ChangeNotifierProvider berubah. Kita harus menentukan tipe data dari state yang akan digunakan. Berikut adalah contoh penggunaan Consumer.

```dart
class HomePage extends StatelessWidget {
  @override
  Widget build(BuildContext context) {
    return Scaffold(
      appBar: AppBar(
        title: Text('Home Page'),
      ),
      body: Center(
        child: Consumer<Counter>(
          builder: (context, counter, child) {
            return Text(
              '${counter.counter}',
              style: TextStyle(fontSize: 24),
            );
          },
        ),
      ),
      floatingActionButton: FloatingActionButton(
        child: Icon(Icons.add),
        onPressed: () {
          Provider.of<Counter>(context, listen: false).increment();
        },
      ),
    );
  }
}
```

Pada contoh di atas, kita membuat widget HomePage yang merupakan child widget dari ChangeNotifierProvider. Widget HomePage memiliki widget Consumer yang digunakan untuk mengambil state yang disediakan oleh ChangeNotifierProvider. Widget Consumer memiliki properti `builder` yang digunakan untuk membuat tampilan widget. Properti `builder` memiliki tiga parameter yaitu `context`, `counter`, dan `child`. Parameter `context` digunakan untuk mengambil state yang disediakan oleh ChangeNotifierProvider. Parameter `counter` digunakan untuk mengambil state yang disediakan oleh ChangeNotifierProvider. Parameter `child` digunakan untuk menentukan widget yang akan ditampilkan ketika state pada ChangeNotifierProvider berubah.

Sebaiknya `Consumer` diletakkan sedalam mungkin agar widget yang tidak membutuhkan state tidak membuat ulang tampilan widgetnya. Jika `Consumer` diletakkan diatas widget yang tidak membutuhkan state, maka widget yang tidak membutuhkan state akan membuat ulang tampilan widgetnya ketika state pada ChangeNotifierProvider berubah.

#### Provider.of

Adakalanya kita membutuhkan state yang disediakan oleh ChangeNotifierProvider di luar widget. Pada kasus tersebut, kita dapat menggunakan fungsi `Provider.of` untuk mengambil state yang disediakan oleh ChangeNotifierProvider. Berikut adalah contoh penggunaan `Provider.of`.

```dart
Provider.of<Counter>(context, listen: false).increment();
```

Pada contoh di atas, kita menggunakan fungsi `Provider.of` untuk mengambil state yang disediakan oleh ChangeNotifierProvider. Fungsi `Provider.of` memiliki dua parameter yaitu `context` dan `listen`. Parameter `context` digunakan untuk mengambil state yang disediakan oleh ChangeNotifierProvider. Parameter `listen` digunakan untuk menentukan apakah widget yang menggunakan state tersebut akan membuat ulang tampilan widgetnya ketika state pada ChangeNotifierProvider berubah. Jika `listen` bernilai `false`, maka widget yang menggunakan state tersebut tidak akan membuat ulang tampilan widgetnya ketika state pada ChangeNotifierProvider berubah.

## Routing

Routing adalah proses untuk mengatur alur navigasi antar halaman. Flutter memiliki fitur routing yang dapat digunakan untuk mengatur alur navigasi antar halaman. Flutter memiliki dua jenis routing yaitu routing dengan menggunakan Navigator dan routing dengan menggunakan PageRouteBuilder.

### Routing dengan menggunakan Navigator

Navigator adalah widget yang digunakan untuk mengatur alur navigasi antar halaman. Navigator memiliki dua jenis yaitu Navigator.push dan Navigator.pushReplacement. Navigator.push digunakan untuk menambahkan halaman baru ke Navigator. Navigator.pushReplacement digunakan untuk mengganti halaman yang sedang ditampilkan dengan halaman baru.

Berikut adalah contoh penggunaan Navigator.push.

```dart
Navigator.push(
  context,
  MaterialPageRoute(
    builder: (context) => SecondPage(),
  ),
);
```

Pada contoh di atas, kita menggunakan Navigator.push untuk menambahkan halaman SecondPage ke Navigator. Navigator.push memiliki dua parameter yaitu `context` dan `MaterialPageRoute`. Parameter `context` digunakan untuk menentukan halaman mana yang akan ditambahkan ke Navigator. Parameter `MaterialPageRoute` digunakan untuk menentukan halaman apa yang akan ditambahkan ke Navigator.

`Navigator` juga dapat digunakan untuk menghapus halaman dari Navigator. Berikut adalah contoh penggunaan Navigator.pop.

```dart
Navigator.pop(context);
```

Pada contoh di atas, kita menggunakan Navigator.pop untuk menghapus halaman yang sedang ditampilkan dari Navigator. Navigator.pop memiliki satu parameter yaitu `context`. Parameter `context` digunakan untuk menentukan halaman mana yang akan dihapus dari Navigator.

### Routing dengan menggunakan PageRouteBuilder

PageRouteBuilder digunakan untuk membuat halaman baru dengan animasi. Berikut adalah contoh penggunaan PageRouteBuilder.

```dart
Navigator.push(
  context,
  PageRouteBuilder(
    pageBuilder: (context, animation, secondaryAnimation) => SecondPage(),
    transitionsBuilder: (context, animation, secondaryAnimation, child) {
      return FadeTransition(
        opacity: animation,
        child: child,
      );
    },
  ),
);
```

Pada contoh di atas, kita menggunakan Navigator.push untuk menambahkan halaman SecondPage ke Navigator. Navigator.push memiliki dua parameter yaitu `context` dan `PageRouteBuilder`. Parameter `context` digunakan untuk menentukan halaman mana yang akan ditambahkan ke Navigator. Parameter `PageRouteBuilder` digunakan untuk menentukan halaman apa yang akan ditambahkan ke Navigator.

PageRouteBuilder memiliki dua properti yaitu `pageBuilder` dan `transitionsBuilder`. Properti `pageBuilder` digunakan untuk menentukan halaman apa yang akan ditambahkan ke Navigator. Properti `transitionsBuilder` digunakan untuk menentukan animasi apa yang akan ditampilkan ketika halaman ditambahkan ke Navigator.

## Fetch Data

Flutter memiliki fitur untuk mengambil data dari API. Flutter memiliki dua jenis widget untuk mengambil data dari API yaitu FutureBuilder dan StreamBuilder. Selain itu, kita juga dapat menggunakan plugin http bawaan dari Flutter untuk mengambil data dari API. Untuk pustaka eksternal lainnya, kita dapat menggunakan plugin Dio. Berikut adalah contoh penggunaan FutureBuilder dan StreamBuilder.

### FutureBuilder

FutureBuilder digunakan untuk menampilkan data yang diambil dari API. Berikut adalah contoh penggunaan FutureBuilder.

```dart
FutureBuilder(
  future: fetchAlbum(),
  builder: (context, snapshot) {
    if (snapshot.hasData) {
      return Text(snapshot.data.title);
    } else if (snapshot.hasError) {
      return Text("${snapshot.error}");
    }

    return CircularProgressIndicator();
  },
);
```

Pada contoh di atas, kita menggunakan FutureBuilder untuk menampilkan data yang diambil dari API. FutureBuilder memiliki dua parameter yaitu `future` dan `builder`. Parameter `future` digunakan untuk menentukan data apa yang akan diambil dari API. Parameter `builder` digunakan untuk menentukan tampilan widget apa yang akan ditampilkan ketika data berhasil diambil dari API.

### StreamBuilder

StreamBuilder digunakan untuk menampilkan data yang diambil dari API secara realtime. Berikut adalah contoh penggunaan StreamBuilder.

```dart
StreamBuilder(
  stream: fetchAlbum(),
  builder: (context, snapshot) {
    if (snapshot.hasData) {
      return Text(snapshot.data.title);
    } else if (snapshot.hasError) {
      return Text("${snapshot.error}");
    }

    return CircularProgressIndicator();
  },
);
```

Pada contoh di atas, kita menggunakan StreamBuilder untuk menampilkan data yang diambil dari API secara realtime. StreamBuilder memiliki dua parameter yaitu `stream` dan `builder`. Parameter `stream` digunakan untuk menentukan data apa yang akan diambil dari API secara realtime. Parameter `builder` digunakan untuk menentukan tampilan widget apa yang akan ditampilkan ketika data berhasil diambil dari API secara realtime.

### http

Plugin http bawaan dari Flutter digunakan untuk mengambil data dari API. Untuk menggunakannya, kita harus menambahkan dependency http pada pubspec.yaml.

```yaml
dependencies:
  http: ^0.13.5
```

Berikut adalah contoh penggunaan plugin http untuk mengambil data dari API.

```dart
Future<Album> fetchAlbum() async {
  final response = await http.get(Uri.parse('https://jsonplaceholder.typicode.com/albums/1'));

  if (response.statusCode == 200) {
    return Album.fromJson(jsonDecode(response.body));
  } else {
    throw Exception('Failed to load album');
  }
}
```

Pada contoh di atas, kita menggunakan plugin http untuk mengambil data dari API. Plugin http memiliki dua method yaitu `get` dan `post`. Method `get` digunakan untuk mengambil data dari API. Method `post` digunakan untuk mengirim data ke API. Method `get` memiliki satu parameter yaitu `Uri`. Parameter `Uri` digunakan untuk menentukan API mana yang akan diakses.

### Dio

Plugin Dio digunakan untuk mengambil data dari API. Untuk menggunakannya, kita harus menambahkan dependency dio pada pubspec.yaml.

```yaml
dependencies:
  dio: ^4.0.6
```

Berikut adalah contoh penggunaan plugin Dio untuk mengambil data dari API.

```dart
Future<Album> fetchAlbum() async {
  final response = await dio.get('https://jsonplaceholder.typicode.com/albums/1');

  return Album.fromJson(response.data);
}
```

Pada contoh di atas, kita menggunakan plugin Dio untuk mengambil data dari API. Plugin Dio memiliki dua method yaitu `get` dan `post`. Method `get` digunakan untuk mengambil data dari API. Method `post` digunakan untuk mengirim data ke API. Method `get` memiliki satu parameter yaitu `url`. Parameter `url` digunakan untuk menentukan API mana yang akan diakses.

Untuk penggunaan post, kita dapat menggunakan method `post` seperti berikut.

```dart
Future<Album> createAlbum(String title) async {
  final response = await dio.post(
    'https://jsonplaceholder.typicode.com/albums',
    data: {'title': title},
  );

  return Album.fromJson(response.data);
}
```

Pada contoh di atas, kita menggunakan plugin Dio untuk mengirim data ke API. Method `post` memiliki dua parameter yaitu `url` dan `data`. Parameter `url` digunakan untuk menentukan API mana yang akan diakses. Parameter `data` digunakan untuk menentukan data apa yang akan dikirim ke API.

## Referensi

  * [https://flutter.dev/](https://flutter.dev/)
  * [https://dart.dev/](https://dart.dev/)
  * [https://www.udemy.com/course/learn-flutter-dart-to-build-ios-android-apps/](https://www.udemy.com/course/learn-flutter-dart-to-build-ios-android-apps/)
  
## Kesimpulan

Flutter adalah framework yang digunakan untuk membuat aplikasi mobile, web, dan desktop. Flutter memiliki dua widget utama yaitu StatelessWidget dan StatefulWidget. StatelessWidget digunakan untuk menampilkan data yang statis. StatefulWidget digunakan untuk menampilkan data yang dinamis. Flutter memiliki dua widget untuk mengambil data dari API yaitu FutureBuilder dan StreamBuilder. Flutter memiliki dua plugin bawaan yaitu http dan Dio. Plugin http digunakan untuk mengambil data dari API. Plugin Dio digunakan untuk mengambil data dari API.

## Tugas

1. Buatlah aplikasi sederhana yang menampilkan data dari API menggunakan FutureBuilder.
2. Buatlah aplikasi sederhana yang menampilkan data dari API secara realtime menggunakan StreamBuilder.
3. Buatlah aplikasi sederhana yang mengirim data ke API menggunakan plugin http.
4. Buatlah aplikasi sederhana yang mengirim data ke API menggunakan plugin Dio.



















