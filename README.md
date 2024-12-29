# Unexpected Equality Comparisons with NaN and -0 in JavaScript

This repository demonstrates an uncommon bug in JavaScript related to loose equality comparisons (==) involving NaN (Not a Number) and -0.

## The Bug

JavaScript's loose equality operator (==) does not work as expected when comparing NaN and -0.

* `NaN == NaN` evaluates to `false`.
* `0 == -0` evaluates to `true`.

This behavior can lead to unexpected results when writing code that checks for equality.

## Code Example

The file `bug.js` demonstrates the problem.  The function `foo` is intended to check if two numbers are equal, but it fails for `NaN` and `-0` values.

## Solution

The file `bugSolution.js` demonstrates a solution using strict equality (===) to avoid these issues.  Strict equality does not perform type coercion and handles NaN and -0 correctly. 

## How to Run

1. Clone this repository.
2. Open `bug.js` and `bugSolution.js` in your preferred JavaScript environment.
3. Run the code and observe the output.
