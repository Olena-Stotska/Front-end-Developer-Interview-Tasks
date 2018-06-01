# Front-end Developer Interview Tasks

This file contains tasks Front-End interview.

I hope, these tasks help fresh developers prepare to interview and for interviewer find potential candidates.

## Tasks on Number

1. Write a function `isPrime()`, which return `true` or `false` if number is prime.

  ```js
  console.log(isPrime(11)) // true
  ```

2. Write a function `factorial()`, which return factorial of the number passed to it.

  ```js
  console.log(factorial(4)) // 24
  console.log(factorial(7)) // 5040
  ```

3. Write a function `fibonacci()`.
    >The Fibonacci sequence is a series of numbers where a number is found by adding up the two numbers before it. Starting with 0 and 1, the sequence goes 0, 1, 1, 2, 3, 5, 8, 13, 21, 34, and so forth. Written as a rule, the expression is xn = xn-1 + xn-2.

  ```js
  console.log(fibonacci(9)) // 21
  ```

4. Write a function `findNextSquare(sq)`, which return the square of the next number and -1, if  the square root of a number is not an integer
  ```js
  console.log(findNextSquare(144)) // 169
  console.log(findNextSquare(155)) // -1 because sqrt(155) = 12.44... (not integer number)
  ```

----

## Tasks on Array

1. Write functions `some()` & `every()` which work as functions `Array.prototype.some()` and `Array.prototype.every()`.

  ```js
  console.log(every([NaN, NaN, NaN], isNaN)) // true
  console.log(every([NaN, NaN, 4], isNaN)) // false
  console.log(some([NaN, 3, 4], isNaN)) // true
  console.log(some([2, 3, 4], isNaN)) // false
  ```

2. Write a function `groupItems()`, which returns an object with keys `even` & `odd` and values are arrays with corresponding numbers.

  ```js
  console.log(groupItems([100, 3, 4, 5, 1, 6, 7])) // { even: [100, 4, 6], odd: [3, 5, 1, 7] }
  ```

3. Write a function `reduce()`, which work as function `Array.prototype.reduce()`, and find sum in array `const items = [1,2,3,4,5,6,7,8,9]`

  ```js
  console.log(reduce(items)) // 45
  ```

4. Write a function that removes duplicate values from an array.

  ```js
  console.log(removeDuplicates([1, 3, 7, 1, 3, 9, 8, 7])) // [1, 3, 7, 9, 8]
  ```

5.  Write a function that returns the common values of two arrays.

  ```js
  console.log(commonValues([3, 4, 6, 3, 1], [5, 10, 7, 1, 3, 9, 8, 7])) // [3, 1]
  ```

6. Write a function that returns the distinct values of two arrays.

  ```js
  console.log(distinctValues([3, 4, 6, 3, 1], [5, 10, 7, 1, 3, 9, 8, 7])) // [4, 6, 5, 10, 7, 9, 8]
  ```

7. Write a function which creates an array with defined size and fills it with random values.

  ```js
  function generateArr(arrSize) {...}
  ```

8. Write your own implementation of Array.prototype.includes() method.

9. You have an array of arrays of unknown deep level. Create a `flatten` function which converts that array to flat array.

  ```js
  console.log(flatten([[1, 2], 5, [ [1], [ [2], [3], [4, 5, 6, 7] ] ], [6, 7]]))
  ```

10. Sort users by age in desc order (bigger is the first)

  ```js
  const users = [{ name: 'John', age: 10 }, { name: 'Peter', age: 12 }, { name: 'Serjio', age: 16 }]
  ```
11. Write a function `map()`, with 2 arguments (array & callback), which work as function `Array.prototype.map()`, and return result `element * index`

  ```js
  console.log(map([1,2,3,4,5,6,7,8,9,10],
                  (element, index, array) => element * index)) // [0, 2, 6, 12, 20, 30, 42, 56, 72, 90]
  ```
12. Write a function `createPhoneNumber()` that return phone number.

  ```js
  console.log(createPhoneNumber([1, 2, 3, 4, 5, 6, 7, 8, 9, 0])) // "(123) 456-7890"
  ```

13. Write a function `groupBy(items, callback)`, which groups the elements by property.

  ```js
  console.log(groupBy([
  {
    firstName: 'Jhon',
    lastName: 'Dou',
    birthYear: 1989,
    isActive: false
  },
  {
    firstName: 'Harry',
    lastName: 'Potter',
    birthYear: 1989,
    isActive: false
  },
  {
    firstName: 'Alan',
    lastName: 'Rickman',
    birthYear: 1994,
    isActive: false,
  },
  {
    firstName: 'Somebody',
    lastName: 'Else',
    birthYear: 1989,
    isActive: true,
  },
  {
    firstName: 'Somebody',
    lastName: 'Man',
    birthYear: 1994,
    isActive: true,
  },
  ], (item, index, array) => [item.isActive])) // { false: [{…}, {…}, {…}], true: [{…}, {…}] }
  ```

  ---

  ## Tasks on DOM

1. Write a function which finds the red bordered node from "structure-1" in "structure-2" (set it the same border) eventually this function should be able to find any mirrored node specified in structure-1

  ```html
    <div id="structure-1">
      <div>
        <div></div>
      </div>
      <div>
        <div></div>
        <div style="border: 3px solid red"></div>
      </div>
      <div>
        <div></div>
        <div></div>
        <div></div>
      </div>
      <div>
        <div></div>
        <div></div>
      </div>
      <div></div>
    </div>

    <div id="structure-2">
      <div>
        <div></div>
      </div>
      <div>
        <div></div>
        <div></div>
      </div>
      <div>
        <div></div>
        <div></div>
        <div></div>
      </div>
      <div>
        <div></div>
        <div></div>
      </div>
      <div></div>
    </div>
  ```

```css
  body {
    display: flex;
  }

  #structure-1,
  #structure-2 {
    border: 3px solid blue;
    width: 200px;
    margin-right: 50px;
  }
  #structure-1 div,
  #structure-2 div {
    min-height: 20px;
  }
  #structure-1 div:empty,
  #structure-2 div:empty {
    background: purple;
  }
  #structure-1 > div,
  #structure-2 > div {
    border: 1px solid #fff;
    margin: 5px;
  }
  #structure-1 > div > div:first-child,
  #structure-2 > div > div:first-child {
    background: #23d6af;
  }
  #structure-1 > div > div:nth-of-type(2),
  #structure-2 > div > div:nth-of-type(2) {
    background: black;
  }
  #structure-1 > div > div:nth-of-type(3),
  #structure-2 > div > div:nth-of-type(3) {
    background: green;
  }

  #structure-2 {
    border-color: lime;
  }
```
  ---

  ## Tasks on ES6

  1. Write a class called Point, which represents a point in two-dimensional space. A point has x and y properties, given as arguments to its constructor.
  It also has a single method plus, which takes another point and returns the sum of the two points, that is, a new point whose x is the sum of the x properties of the two original points, and whose y is the sum of their y properties.

  ```js
  console.log(new Point(1, 2).plus(new Point(2, 1))) // Point{x: 3, y: 3}
  ```

  2.
