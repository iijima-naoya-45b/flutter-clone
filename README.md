# flutter-clone
fluitter-clone用

作成する際には、組織名がないとAppStoreにアップできないので注意

```
flutter create --org com.yourcompany（組織名） app_name
```

### IOS 

下記cmd打鍵後に、実行deviceを選択
```
flutter run
```

iosエミュレーター起動する場合
```
flutter emulators --launch apple_ios_simulator
```


## `Tips`

✅ Android の組織変更方法

1. android/app/src/main/AndroidManifest.xml の修正
(パッケージ名を変更)
```
<manifest xmlns:android="http://schemas.android.com/apk/res/android"
    package="com.example.my_app">
```

2.android/app/build.gradle の修正
→ 新しい ID に：

```
defaultConfig {
    applicationId "com.example.my_app"
}
```


3．パッケージ名に対応したディレクトリ名を変更
(Java/Kotlinファイルの package 宣言も修正：)
```
android/app/src/main/java/com/example/my_app/
↓
android/app/src/main/java/com/mycompany/my_app/

package com.example.my_app;
↓
package com.mycompany.my_app;
```

✅ iOS の変更方法

ios/Runner.xcodeproj/project.pbxproj を開いて PRODUCT_BUNDLE_IDENTIFIER を検索して修正
```
PRODUCT_BUNDLE_IDENTIFIER = com.example.myApp;
↓
PRODUCT_BUNDLE_IDENTIFIER = com.mycompany.myApp;
```
