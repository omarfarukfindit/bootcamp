# Typedef in Dart

A `typedef` in Dart allows you to create a custom name for a function type. This is extremely helpful for improving code readability, especially when using callbacks or multiple functions with the same signature.

## Use Case: Validators

```dart
typedef Validator = String? Function(String input);

String? nonEmptyValidator(String input) {
  return input.isEmpty ? 'Input cannot be empty' : null;
}

String? emailValidator(String input) {
  return input.contains('@') ? null : 'Invalid email format';
}

void validateInput(String value, List<Validator> rules) {
  for (var rule in rules) {
    final error = rule(value);
    if (error != null) {
      print('Validation failed: $error');
      return;
    }
  }
  print('Validation passed.');
}

void main() {
  final input = 'test@example.com';
  validateInput(input, [nonEmptyValidator, emailValidator]);
}
```

## Benefits

* Makes function signatures **easier to manage**
* Improves **maintainability** and **documentation**

---
