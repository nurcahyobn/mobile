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

//class Mahasiswa   

//class Dosen 
```


```dart
    routes: {
      '/mahasiswa': (BuildContext context) => Mahasiswa(),
      '/dosen': (BuildContext context) => Dosen(),
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
