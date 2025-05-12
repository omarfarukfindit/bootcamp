# Higher-Order Functions in Dart

A higher-order function is a function that can accept another function as a parameter, or return a function as its result. In Dart, functions are first-class objects — this means you can pass them around just like variables.

## 🔧 Use Case: Wrapping Functionality

```dart
void logAction(String message, void Function() action) {
  print('Start: $message');
  action();
  print('End: $message');
}

void main() {
  logAction('Saving data', () {
    print('Data saved to database.');
  });

  logAction('Syncing with server', () {
    print('Server sync complete.');
  });
}
```

## Benefits

* Promotes **code reuse**
* Useful in **middleware**, **event handling**, and **custom control flows**

---
