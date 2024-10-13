import 'package:flutter/material.dart';

void main() {
  runApp(MyApp());
}

class MyApp extends StatefulWidget {
  @override
  _MyAppState createState() => _MyAppState();
}

class _MyAppState extends State<MyApp> {
  bool isYellow = true;

  void _changeColor() {
    setState(() {
      isYellow = !isYellow;
    });
  }

  @override
  Widget build(BuildContext context) {
    return MaterialApp(
      home: Scaffold(
        backgroundColor: isYellow ? Colors.yellow : Colors.blue,
        body: Center(
          child: ElevatedButton(
            onPressed: _changeColor,
            child: Text('Rengi Değiştir'),
          ),
        ),
      ),
    );
  }
}
