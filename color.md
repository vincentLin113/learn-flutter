# How to use gradient with Flutter?

```dart
class _GradientPractice extends State<GradientPractice>{
  List<Color> _colors = [Colors.deepOrange, Colors.yellow];
  List<double> _stops = [0.0, 0.7];

  @override
  void initState() {
    super.initState();
  }

  @override
  Widget build(BuildContext context) {
    return MaterialApp(
      home: Center(
        child: Container(
          height: 200,
          width: 200,
          decoration: BoxDecoration(
              gradient: LinearGradient(
                colors: _colors,
                stops: _stops,
              )
          ),
        ),
      ),
    );
  }
}
```

## Ref: https://medium.com/@erdoganbavas/gradients-in-flutter-4677cbe1587b
