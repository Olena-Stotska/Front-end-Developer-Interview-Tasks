# Front-end Developer Interview Tasks

This file contains tasks Front-End interview.

I hope, these tasks help fresh developers prepare to interview and for interviewer find potential candidates.

## Tasks on Number

1. Write a function `isPrime()`, which return `true` or `false` if number is prime

  ```js
  console.log(isPrime(11)) // true
  ```

2. Write a function `factorial()`, which return factorial of the number passed to it

  ```js
  console.log(factorial(4)) // 24
  console.log(factorial(7)) // 5040
  ```

3. Write a function `fibonacci()`
    >The Fibonacci sequence is a series of numbers where a number is found by adding up the two numbers before it. Starting with 0 and 1, the sequence goes 0, 1, 1, 2, 3, 5, 8, 13, 21, 34, and so forth. Written as a rule, the expression is xn = xn-1 + xn-2.

  ```js
  console.log(fibonacci(9)) // 21
  ```

----

## Tasks on Array

1. Write functions `some()` & `every()` which work as functions `Array.prototype.some()` and `Array.prototype.every()`

  ```js
  console.log(every([NaN, NaN, NaN], isNaN)) // true
  console.log(every([NaN, NaN, 4], isNaN)) // false
  console.log(some([NaN, 3, 4], isNaN)) // true
  console.log(some([2, 3, 4], isNaN)) // false
  ```

2. Write a function `groupItems()`, which returns an object with keys `even` & `odd` and values are arrays with corresponding numbers

  ```js
  console.log(groupItems([100, 3, 4, 5, 1, 6, 7])) // { even: [100, 4, 6], odd: [3, 5, 1, 7] }
  ```

3. Write a function `reduce()`, which work as function `Array.prototype.reduce()`, and find sum in array `const items = [1,2,3,4,5,6,7,8,9]`

  ```js
  console.log(reduce(items)) // 45
  ```

----
