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

##### REST API call asynchronous

```dart
FutureBuilder(
      // Future should be the Future class or the "action" you want to execute and waiting until it has been completed.
      // In this case it is calling a REST API using the http package.
      future: url != null
          ? http.get("http://given_host/api/given_service").then((response) => response.body)
          : null,
      builder: (BuildContext context, AsyncSnapshot<String> snapshot) {
        switch (snapshot.connectionState) {
          // In case of no URL
          case ConnectionState.none:
            return new Text('No URL informed');
          // In case of REST request is been processed
          case ConnectionState.waiting:
            return new Center(child: new CircularProgressIndicator());
          // In case of connection is active
          case ConnectionState.active:
            return new Text('active');
          case ConnectionState.done:
            // Request is done but with error
            if (snapshot.hasError) {
              return new Text(
                '${snapshot.error}',
                style: TextStyle(color: Colors.red),
              );
            // Request is done and was successful executed
            } else {
              return Text(jsonDecode(snapshot.data));
            }
        }
      }
  ),
```
