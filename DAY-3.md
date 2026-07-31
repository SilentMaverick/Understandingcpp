# DAY-3 — Loops and Conditionals (if/else, for, while, do-while, continue, break)

This lesson covers conditional statements and loops in C++ with simple examples and practice questions.

## 1. if / else
Use if and else to run code conditionally.

Example:
```cpp
#include <iostream>
using namespace std;

int main() {
    int x;
    cout << "Enter an integer: ";
    cin >> x;

    if (x > 0) {
        cout << x << " is positive\n";
    } else if (x < 0) {
        cout << x << " is negative\n";
    } else {
        cout << "You entered zero\n";
    }
    return 0;
}
```

Tips:
- Conditions evaluate to true or false.
- Use `==` to compare, `=` is assignment.
- Combine conditions with `&&` (and), `||` (or), and `!` (not).

## 2. for loop
Use `for` when you know how many times the loop should run.

Syntax:
```cpp
for (initialization; condition; update) {
    // body
}
```

Example — print first 10 natural numbers:
```cpp
for (int i = 1; i <= 10; ++i) {
    cout << i << " ";
}
cout << '\n';
```

## 3. while loop
Use `while` when the number of iterations depends on a condition checked before each iteration.

Example — read numbers until user enters 0:
```cpp
int n;
while (cin >> n && n != 0) {
    cout << "You entered: " << n << '\n';
}
```

## 4. do-while loop
`do-while` runs the body at least once, then checks the condition.

Example — ask user to continue:
```cpp
char again;

do {
    cout << "Running once...\n";
    cout << "Another time? (y/n): ";
    cin >> again;
} while (again == 'y' || again == 'Y');
```

## 5. continue and break
- `continue` skips the rest of the current loop iteration and proceeds to the next iteration.
- `break` exits the loop immediately.

Example — show usage:
```cpp
// print odd numbers from 1 to 10 using continue
for (int i = 1; i <= 10; ++i) {
    if (i % 2 == 0) continue; // skip even
    cout << i << " ";
}
cout << '\n';

// find first multiple of 7 between 1 and 100
for (int i = 1; i <= 100; ++i) {
    if (i % 7 == 0) {
        cout << "First multiple of 7 is " << i << '\n';
        break; // stop the loop
    }
}
```

## Common pitfalls
- Infinite loops: ensure the loop condition will eventually become false or use `break` carefully.
- Off-by-one errors: pay attention to `<=` vs `<` and starting index.
- Using assignment `=` instead of comparison `==` in conditions.

---

## Practice Questions
Grouped by difficulty. Try to implement these in C++ and test with different inputs.

Easy
1. Write a program that reads an integer n and prints the sum of numbers from 1 to n using a for loop.
2. Read integers until the user inputs -1; print how many numbers were entered (exclude the -1). Use a while loop.
3. Print all even numbers between 1 and 50 using a for loop and `continue`.

Medium
4. Read an integer n and print the factorial of n using a loop. (Assume n >= 0; use `long long` for larger values.)
5. Check if a given number is prime. Use a loop that stops early when a divisor is found (use `break`).
6. Given a list of integers (read until 0), print the maximum and minimum values.

Hard
7. FizzBuzz variant: For numbers from 1 to n, print "Fizz" for multiples of 3, "Buzz" for multiples of 5, and "FizzBuzz" for multiples of both. Do this using a single loop and avoid unnecessary checks.
8. Find the first number in the Fibonacci sequence with at least k digits. Use a loop and stop when the condition is met.
9. Given a matrix (n x m), read values and find the row with the largest sum. Use nested loops.

Challenge / Thinking questions
10. Without using multiplication or division operators, compute n * m using only addition and loops. Consider which loop is more efficient based on which number is larger.
11. Explain why a do-while loop is useful for input validation when you must ask the user at least once.
12. Given two sorted arrays, use loops to merge them into a single sorted array (like the merge step in merge sort). What is the time complexity?

---

If you want, I can also:
- Add solutions for the practice problems in a separate file (DAY-3-solutions.md).
- Put this lesson into a `lessons/` folder or `docs/` and update the README with links.

Happy coding — practice these until they're second nature!
