# DAY-3 Assignment — Loops & Conditionals

Instructions:
- Solve the problems using C++ and create separate .cpp files for each solution if you like.
- Add comments explaining your approach and the time complexity where relevant.
- Test your programs with multiple inputs and edge cases.

Problems

1) Sum of Evens (Easy)
- Read an integer n (n >= 1). Print the sum of all even numbers from 1 to n.
- Sample:
  Input: 10
  Output: 30

2) Count Until Sentinel (Easy)
- Read integers until -1 is entered. Output the count of numbers read (excluding -1).
- Example: Input: 3 5 7 -1 -> Output: 3

3) Reverse Digits (Medium)
- Read a positive integer and print its digits in reverse order using a loop (do not convert to string).
- Input: 12345 -> Output: 54321

4) Smallest Divisor (Medium)
- Given an integer n > 1, find its smallest divisor greater than 1. Use a loop and stop early when found.
- Input: 91 -> Output: 7

5) Sum of Factorials (Medium)
- Read an integer n (1 <= n <= 10). Compute S = 1! + 2! + ... + n! using loops.

6) First Repeated Number (Hard)
- Read integers until 0. Find and print the first number that repeats (i.e., the first value that has already appeared earlier). If none repeat, print "No repetition".

7) Matrix Column Max (Hard)
- Read integers n and m, then an n x m matrix. Print the maximum value of each column (m numbers).

8) Game Simulation (Hard)
- Simulate a simple game: a player starts with score 0. Read commands until "END". Commands:
  - "ADD x" -> add x to score
  - "SUB x" -> subtract x
  - "SKIP" -> skip next command (use continue/logic)
  - "STOP" -> end processing (use break)
- Print final score after processing commands.

9) Efficient Multiplication (Challenge)
- Implement multiplication of two non-negative integers using repeated addition in O(min(n,m)) iterations by looping over the smaller multiplier.

Submission
- Create a folder DAY-3/solutions/ and add your solution files named by problem number (e.g., 1_sum_of_evens.cpp).
- Optionally add a README in DAY-3/ describing how to compile and run solutions.

Optional: Push your solutions in a separate branch and open a PR for review.
