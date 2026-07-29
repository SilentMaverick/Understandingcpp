# Day 2 — Operators (Easy Explanations + Examples)

This page explains common C++ operators in the easiest way possible, with short examples you can try.

---

## 1) Implicit Type Conversion (automatic)
What it is: The compiler automatically converts one type to another when needed (also called "type promotion").

Why it matters: This is convenient but can surprise you (e.g., losing fractional part).

Example:
```cpp
#include <iostream>
int main() {
    double d = 3.7;
    int i = d;           // implicit conversion: double -> int (fraction lost)
    std::cout << i << "\n"; // prints 3
    
    int a = 5;
    double b = 2.0;
    double c = a / b;   // a implicitly converted to double: 5.0 / 2.0 = 2.5
    std::cout << c << "\n"; // prints 2.5
}
```
Tip: When both operands are integers, integer division happens (fraction discarded). If one operand is floating-point, the result becomes floating-point.

---

## 2) Explicit Type Conversion (casting)
What it is: You tell the compiler to convert a value to another type.

How to do it safely: use `static_cast<T>(value)` instead of C-style casts.

Examples:
```cpp
#include <iostream>
int main() {
    double d = 3.7;
    int i = static_cast<int>(d); // explicit conversion: round toward zero -> 3
    std::cout << i << "\n";

    int a = 5, b = 2;
    double r = static_cast<double>(a) / b; // 5.0 / 2 = 2.5
    std::cout << r << "\n";
}
```
When to use: when implicit conversion would lose data or you need a specific type for an operation.

---

## 3) Arithmetic Operators
What they do: perform math on numbers.

Common operators: `+`, `-`, `*`, `/`, `%` (remainder)

Example:
```cpp
#include <iostream>
int main() {
    int x = 7, y = 3;
    std::cout << "x + y = " << (x + y) << "\n"; // 10
    std::cout << "x - y = " << (x - y) << "\n"; // 4
    std::cout << "x * y = " << (x * y) << "\n"; // 21
    std::cout << "x / y = " << (x / y) << "\n"; // 2 (integer division)
    std::cout << "x % y = " << (x % y) << "\n"; // 1
}
```
Note: with floating-point types, `/` gives fractional results; `%` works only with integers.

---

## 4) Unary Operators
What they do: operate on a single value.

Common unary operators: `+` (unary plus), `-` (negation), `++` (increment), `--` (decrement), `!` (logical NOT)

Examples:
```cpp
#include <iostream>
int main() {
    int a = 5;
    std::cout << ++a << "\n"; // pre-increment: a becomes 6, prints 6

    a = 5;
    std::cout << a++ << "\n"; // post-increment: prints 5, then a becomes 6

    int b = -a;                // unary -: negate value
    bool ok = !(a == 6);       // logical NOT: !(true) -> false
    std::cout << b << " " << std::boolalpha << ok << "\n";
}
```
Tip: pre-increment (`++x`) changes value before using it; post-increment (`x++`) uses the old value then increments.

---

## 5) Relational Operators
What they do: compare values and return `true` or `false`.

Operators: `==` (equal), `!=` (not equal), `<`, `>`, `<=`, `>=`

Example:
```cpp
#include <iostream>
int main() {
    int a = 5, b = 3;
    std::cout << (a == b) << "\n"; // 0 (false)
    std::cout << (a != b) << "\n"; // 1 (true)
    std::cout << (a > b) << "\n";  // 1 (true)
}
```
Use relational operators in `if` statements, loops, and expressions that test conditions.

---

## 6) Logical Operators
What they do: combine boolean expressions.

Operators: `&&` (AND), `||` (OR), `!` (NOT)

Short-circuit behavior: `&&` stops evaluating if the left side is false; `||` stops if the left side is true.

Example:
```cpp
#include <iostream>
int main() {
    int x = 5;
    bool test = (x > 0) && (x < 10); // true if x is between 0 and 10
    std::cout << std::boolalpha << test << "\n"; // prints true

    bool either = (x == 5) || (x == 6);
    std::cout << either << "\n"; // true

    std::cout << !(x == 0) << "\n"; // true, because x is not zero
}
```

When to combine: use relational ops to create boolean conditions, then combine them with logical ops to express more complex checks.

---

## Quick Summary (one-line cheats):
- Implicit conversion: compiler quietly changes types (watch for lost fractions).
- Explicit conversion: you force the change with `static_cast<T>(value)`.
- Arithmetic: `+ - * / %` (note integer vs float division).
- Unary: `+ - ++ -- !` (single operand; pre vs post matters for ++/--).
- Relational: `== != < > <= >=` (compare values -> bool).
- Logical: `&& || !` (combine boolean tests; short-circuits).

Happy coding — try the examples and change values to see results!
