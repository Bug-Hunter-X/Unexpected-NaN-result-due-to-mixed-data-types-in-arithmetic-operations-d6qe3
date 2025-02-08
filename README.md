# Unexpected NaN result due to mixed data types in arithmetic operations

This repository demonstrates a common JavaScript bug caused by the language's loose typing system. When performing arithmetic operations, mixing strings and numbers can lead to unexpected `NaN` (Not a Number) results.

## Bug Description
The `bar` function calls `foo`, which performs addition. When `bar` receives a string and a number as input, the addition in `foo` leads to type coercion.  The resulting value is a string, and subsequent multiplication in `bar` results in `NaN`.

## Bug Reproduction
1. Clone this repository.
2. Open `bug.js`.
3. Run the JavaScript code using Node.js or a browser's developer console.
4. Observe the unexpected `NaN` output.

## Solution
The solution involves explicit type checking and conversion before performing arithmetic operations. This ensures that all values are of the correct type before calculations, thus preventing `NaN` values.