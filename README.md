# JavaScript Loose Equality Bug

This repository demonstrates a common JavaScript bug related to loose equality (==) when handling null and undefined values.

## Description
The `foo` function intends to return 0 if the input `x` is null and `x + 1` otherwise. However, due to loose equality, `undefined` is also treated as 0, leading to unexpected NaN when `undefined` is passed.

## How to Reproduce
1. Clone this repository.
2. Open `bug.js` and run it using a JavaScript runtime (Node.js, browser console, etc.).

## Solution
The `bugSolution.js` file provides a corrected version using strict equality (===) to prevent this issue. This ensures that only strict null checks are performed, avoiding the confusion with undefined values.

## Lessons Learned
Always use strict equality (===) when comparing values in JavaScript to avoid unexpected behavior with loose equality (==), especially when dealing with null and undefined.