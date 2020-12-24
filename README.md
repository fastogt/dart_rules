## Analysis

Add `dart_rules` as dependency to your pubspec.yaml

```yaml
dev_dependencies:
  dart_rules: ^1.0.0
```

Add a `analysis_options.yaml` to the root of you project.

```yaml
include: package:dart_rules/analysis_options.yaml
```

Hit save and see the `dartanalyzer` executing the lint checks in you favorite editor.

If a specific lint warning should be ignored, it can be flagged with a comment. For example,

```dart
   // ignore: avoid_as
   (pm as Person).firstName = 'Seth';
```

tells the Dart analyzer to ignore this instance of the `avoid_as` warning.

End-of-line comments are supported as well. The following communicates the same thing:

```dart
   (pm as Person).firstName = 'Seth'; // ignore: avoid_as
```

To ignore a rule for an entire file, use the `ignore_for_file` comment flag. For example,

```dart
// ignore_for_file: avoid_as

void main() {
  ...
  (pm as Person).firstName = 'Seth';
}
```

tells the Dart analyzer to ignore all occurrences of the `avoid_as` warning in this file.

## Formatting

To format all files in project run `flutter format . --line-length=100`.

To format your code in the current source code window use the following:

#### Android Studio:

`Cmd+Alt+L` (on Mac) or `Ctrl+Alt+L` (on Windows and Linux).

#### VS Code:

`Shift+Alt+А` or right-click in the code window and select `Format Document`

## Style

Set maximum line length to 100 symbols
On both `Android Studio` and `VS Code` do

```
File -> Settings -> Input in search bar 'line length dart'
```

#### Android Studio:

![](https://i.imgur.com/xWZ6lly.jpg)

#### VS Code:

![](https://i.imgur.com/GQY5h3m.jpg)
