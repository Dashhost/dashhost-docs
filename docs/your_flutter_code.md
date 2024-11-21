# Your Flutter Code

## Important Notes

### URL Routing
For Dashhost to work to it's full potential, your navigation shouldn't use hashbangs (`/#/`) in the URL bar. This can be easily fixed by [modifying your URL strategy](https://docs.flutter.dev/ui/navigation/url-strategies). 

```yaml
# pubspec.yaml
dependencies:
  flutter:
    sdk: flutter
  flutter_web_plugins:
    sdk: flutter
```

```bash
# run in terminal
flutter pub get
```

```dart
// main.dart
import 'package:flutter_web_plugins/url_strategy.dart';

void main() {
  usePathUrlStrategy();
  runApp(ExampleApp());
}
```


### Non version-controlled files

Since Dashhost needs all your code to run a build, you will run into problems if some files are not version controlled. 

A common issue is if you have your `firebase_options.dart` and you've followed the docs which say not to version control this.

The better approach is to rely on **environment variables** so that your keys are not version controlled (which can be annoying if you have multiple environments).

```dart
static const FirebaseOptions web = FirebaseOptions(
    apiKey: const String.fromEnvironment("FIREBASE_API_KEY"),
    appId: const String.fromEnvironment("FIREBASE_APP_ID"),
    //... and so forth
  );
```

Note: you MUST have `const` before each environment line.

Then, simply add these variables to your app through Dashhost's environment variables manager.

#### Continuing work on your app locally

Since locally you won't have these variables automatically, we recomend setting them in your `.vscode/launch.json` or using a package like [flutter_dotenv](https://pub.dev/packages/flutter_dotenv) to manage your local environment.