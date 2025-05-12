# Anonymous Functions in Dart

An anonymous function is a function without a name. In Dart, they’re often used as inline functions — especially helpful when the logic is short and used only once.

## Use Case 1: Filtering a List

```dart
void main() {
  final numbers = [1, 5, 8, 10, 13];

  final evenNumbers = numbers.where((n) {
    return n % 2 == 0;
  }).toList();

  print('Even numbers: $evenNumbers');
}
```

## Use Case 2: Sorting a List

```dart
void main() {
  final items = ['banana', 'apple', 'mango'];

  items.sort((a, b) => a.compareTo(b));
  print('Sorted items: $items');
}
```

## Benefits

* Keeps code **concise and clean**
* Reduces clutter when logic is only needed temporarily

---
