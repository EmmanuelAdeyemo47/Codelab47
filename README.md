# Codelab47: flutter Business Card:

import 'package:flutter/material.dart';

void main() {
  runApp(MyApp());
}

class MyApp extends StatelessWidget {
  @override
  Widget build(BuildContext context) {
    return MaterialApp(
      home: Scaffold(
        backgroundColor: Colors.teal,
        body: SafeArea(
            child: Column(
          mainAxisAlignment: MainAxisAlignment.center,
          children: <Widget>[
            CircleAvatar(
              radius: 50.0,
              backgroundImage: AssetImage("images/Emma..png"),
            ),
            Text('Emmanuel Adeyemo',
                style: TextStyle(
                    fontFamily: 'Pacifico',
                    fontSize: 20.0,
                    color: Colors.white,
                    fontWeight: FontWeight.bold)),
            Text('FLUTTER DEVELOPER',
                style: TextStyle(
                    fontFamily: 'Source Sans Pro',
                    fontSize: 20.0,
                    color: Colors.teal.shade100,
                    fontWeight: FontWeight.bold,
                    letterSpacing: 2.5)),
            SizedBox(
              height: 20.0,
              width: 150.0,
              child: Divider(
                // HERE we will add a divider
                color: Colors.teal.shade100,
              ),
            ),
            Card(
                // color: Colors.white,
                margin: EdgeInsets.symmetric(vertical: 10.0, horizontal: 10.0),
                child: ListTile(
                  leading: Icon(
                    //Icons.add_shopping_cart,
                    Icons.phone,
                    color: Colors.teal,
                  ),
                  title: Text('+1 123 456 7890',
                      style: TextStyle(
                        color: Colors.teal.shade900,
                        fontFamily: 'Source Sans Pro',
                        fontSize: 20.0,
                      )),
                )),
            Card(
              //color: Colors.white,
              margin: EdgeInsets.symmetric(vertical: 10.0, horizontal: 10.0),
              child: Padding(
                  padding: EdgeInsets.all(5.0),
                  child: ListTile(
                    leading: Icon(
                      Icons.email,
                      color: Colors.teal,
                    ),
                    title: Text(
                      'example@gmail.com',
                      style: TextStyle(
                        color: Colors.teal.shade900,
                        fontFamily: 'Source Sans Pro',
                        fontSize: 18.0,
                      ),
                    ),
                  )),
            ),
          ],
        )),
      ),
    );
  }
}

