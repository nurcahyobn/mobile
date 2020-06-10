# Membuat Navigasi dan Routes

```dart
import 'package:flutter/material.dart';

void main() {
  runApp(new MaterialApp(
    debugShowCheckedModeBanner: false,

    home: new HomePage(),
    //Mendefinisikan Routing yang mengatur halaman app
  ));
}

class HomePage extends StatelessWidget {
  Widget build(BuildContext context) {
    return new Scaffold(
        appBar: new AppBar(
          title: new Text("HomePage"),        
        ),
        body: Center(
          child: Text('Halaman Utama', style: TextStyle(fontSize: 32)),
        ));
  }
}

//class MahasiswaPage   

//class DosenPage 
```


```dart
    routes: {
      '/mahasiswa': (BuildContext context) => MahasiswaPage(),
      '/dosen': (BuildContext context) => DosenPage(),
    },
```


```dart
        actions: <Widget>[
            IconButton(
                icon: Icon(Icons.face),
                tooltip: 'Mahasiswa',
                onPressed: () {
                  Navigator.of(context).pushNamed("/mahasiswa");
                }),
            IconButton(
                icon: Icon(Icons.account_box),
                tooltip: 'Dosen',
                onPressed: () {
                  Navigator.of(context).pushNamed("/dosen");
                }),
          ],
```        

> Quis: 

* title: new Text("HomePage"), #`HomePage` ganti `NAMA Mahasiswa`
* Halaman `Mahasiswa` : data Mahasiswa menggunakan ListView (Pert-14)
* Halaman `Dosen` : data Dosen menggunakan ListView (Pert-14)

![Tampilan Awal](/tugas-nav.gif)
