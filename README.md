# Program Aritmatika

> `Step-1` : Membuat Layout `StatelessWidget`

```dart
import 'package:flutter/material.dart';

void main() => runApp(App09());

class App09 extends StatelessWidget {
  Widget build(BuildContext context) {
    return MaterialApp(
      title: 'Program Persegi Panjang',
      home: Scaffold(
        appBar: AppBar(
          title: Text('Nurcahyo (KELAS)'),
        ),
        body: Text("Step-1"),
      ),
    );
  }
}
```

> `Step-2` : Membuat Layout `StatefulWidget`
- ubah kode `body: MyApp(),`
- tambah perintah dibawah untuk `class MyApp()`
  
```dart
class MyApp extends StatefulWidget {
  _MyAppState createState() => _MyAppState();
}

class _MyAppState extends State<MyApp> {
  Widget build(BuildContext context) {
    return Center(
      child: Text("Step-2"),
    );
  }
}
```

> `Step-3` : Membuat Layout Container, RaisedButton
- ubah `return Center` pada `step-2`

```dart
return Center(
    child: Column(
        mainAxisAlignment: MainAxisAlignment.center,
        children: <Widget>[
        Container(
            width: 280,
            padding: EdgeInsets.all(10.0),
            color: Colors.yellow,
            child: Text("Input panjang"),
        ),
        Container(
            width: 280,
            padding: EdgeInsets.all(10.0),
            color: Colors.green,
            child: Text("Input lebar"),
        ),
        RaisedButton(
            child: Text('Hitung Luas'), 
            onPressed: () {},
        ),
        Container(
            width: 280,
            padding: EdgeInsets.all(10.0),
            color: Colors.green,
            child: Text("Luas Persegi"),
        ),
        ]),
);
```
> `Step-4` : Deklarasi `variabel` dan `fungsi` klik Button Hitung

```dart
class _MyAppState extends State<MyApp> {
  final txtpanjang = TextEditingController();
  final txtlebar = TextEditingController();

  String hasil = '';

  onHitung() {
    setState(() {
      var panjang = int.parse(txtpanjang.text);
      var lebar = int.parse(txtlebar.text);
      var luas = panjang * lebar;
      hasil = luas.toString();
    });
  }

  Widget build(BuildContext context) {
  ...
```

> `Step-5` : Widget input `TextField`

- hapus semua attribut `color` (contoh: `color: Colors.green,`)
- ubah widget `Text` dengan `TextField`

```dart
child: TextField(
    controller: txtpanjang,
    autocorrect: true,
    decoration: InputDecoration(hintText: 'Input Panjang'),
),
```

> berikut kode `return Center`

![a](/step1.png)

![a](/step2.png)
