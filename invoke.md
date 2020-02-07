## How to use invoke

## Flutter
```dart
  static const platform = const MethodChannel('flutter_client');
  
  // Send message to specific platform
  await platform.invokeListMethod("CLOSE");
```

## Swift
```swift
let closeChannel = FlutterMethodChannel(name: "flutter_client", binaryMessenger: flutterViewController.binaryMessenger)
closeChannel.setMethodCallHandler { (call, result) in
if (call.method == "CLOSE") {
    flutterViewController.dismissSelf()
   }
}
```
