Add `dart_rules` as dependency to your pubspec.yaml

```yaml
dev_dependencies:
  dart_rules: ^1.3.0
```

Add a `analysis_options.yaml` to the root of you project.

```yaml
include: package:dart_rules/analysis_options.yaml
```

Hit save and see the `dartanalyzer` executing the lint checks in you favorite editor.

If a specific lint warning should be ignored, it can be flagged with a comment.  For example, 

```dart
   // ignore: avoid_as
   (pm as Person).firstName = 'Seth';
```

tells the Dart analyzer to ignore this instance of the `avoid_as` warning.

End-of-line comments are supported as well.  The following communicates the same thing:

```dart
   (pm as Person).firstName = 'Seth'; // ignore: avoid_as
```

To ignore a rule for an entire file, use the `ignore_for_file` comment flag.  For example,

```dart
// ignore_for_file: avoid_as

void main() {
  ...
  (pm as Person).firstName = 'Seth';
}
```

tells the Dart analyzer to ignore all occurrences of the `avoid_as` warning in this file.