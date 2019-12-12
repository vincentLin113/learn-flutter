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
