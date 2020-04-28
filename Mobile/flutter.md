# Flutter

### Usefull command line

```shell
# Build an APK
cd <app dir>
flutter build apk --split-per-abi
```

### Important concepts

##### Add app permision on AndroidManifest.xml file to access the internet when the apk build is deployed on a Android device
```xml
<uses-permission android:name="android.permission.INTERNET"/>
```
