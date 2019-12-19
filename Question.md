# 常見問題

### Command PhaseScriptExecution failed with a nonzero exit code while trying to add Flutter to iOS app
[回答集](https://github.com/flutter/flutter/issues/23465)
The same compiling error occurred for me.
But i solved it by switching channel to master.
```
Flutter channel master
```
Then delete the old module and recreate it by
```
flutter create -t module my_flutter
```
Next
```
pod install
```
Finally, clean the xcode project, restart Xcode, Cmd+B the error disappeared.

---

### 當Flutter找不到你想要的simulator或Real device
[回答集](https://github.com/flutter/flutter/issues/41006)  
```
rm -rf <flutter_repo_directory>/bin/cache
```
flutter_repo_directory不是指向專案，而是flutter sdk存取的地方


---

### The method 'CachedNetworkImageProvider.load' has fewer positional arguments than those of overridden method 'ImageProvider.load'
[回答集](https://stackoverflow.com/questions/59304169/cachednetworkimage-throwing-error-after-upgrading-to-latest-flutter-stable-versi)  
0

As mentioned in the official page

Breaking change with ImageProvider.load in Flutter 1.10

The Flutter team made a breaking change with the ImageProvider in Flutter 1.10.15 (currently Master channel only).

If you are experiencing one of the following errors upgrade to 2.0.0-rc.

switch to cached_network_image: ^2.0.0-rc

If the issue still persists then try flutter clean and run.

1. 進去你的flutter project
2. 開啟pubspec.yaml
3. 修改cachedNetworkImage的版本
(版本說明及更新方式)[https://pub.dev/packages/cached_network_image/versions/2.0.0-rc#-installing-tab-]
