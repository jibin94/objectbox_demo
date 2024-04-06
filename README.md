## What is ObjectBox?
ObjectBox is a NoSQL database for Flutter built for speed and simplicity. It throws away the clunky SQL schema and lets you directly store your Dart objects — no messy migrations or mappings needed.

### Getting started with ObjectBox
To add ObjectBox to your Flutter project:
Run these commands:
```
flutter pub add objectbox objectbox_flutter_libs:any
flutter pub add --dev build_runner objectbox_generator:any
```
This should add lines like this to your pubspec.yaml:
```
dependencies:
  objectbox: any
  objectbox_flutter_libs: any

dev_dependencies:
  build_runner: ^any
  objectbox_generator: any
```
### Generate ObjectBox code
Run ```flutter pub run build_runner build``` to generate the binding code required to use ObjectBox.
ObjectBox generator will look for all ```@Entity``` annotations in your lib folder and create a single database definition ```lib/objectbox-model.json``` and supporting code in ```lib/objectbox.g.dart```.
