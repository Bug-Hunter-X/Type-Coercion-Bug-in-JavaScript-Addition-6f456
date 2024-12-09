# JavaScript Type Coercion Bug

This repository demonstrates a subtle bug in JavaScript related to type coercion when using the loose equality operator (==) in combination with the addition operator (+).

## The Bug

The `foo` function is designed to add two numbers. However, it contains a flaw in its null check.  If either parameter is 0, it will be treated as falsy and return 0 instead of performing the addition. This is because loose equality (==) does type coercion.

## The Solution

The solution utilizes strict equality (===) to avoid type coercion, ensuring that only null values are correctly handled. 