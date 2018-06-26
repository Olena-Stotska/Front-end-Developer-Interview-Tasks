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
    >The Fibonacci sequence is a series of numbers where a number is found by adding up the two numbers before it.
    Starting with 0 and 1, the sequence goes 0, 1, 1, 2, 3, 5, 8, 13, 21, 34, and so forth. Written as a rule, the expression is xn = xn-1 + xn-2.

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

3. Write a function `reduce()`, which work as function `Array.prototype.reduce()`, and find sum in array
   `const items = [1,2,3,4,5,6,7,8,9]`

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

14. Accounting

    Write an expression using higher-order array methods (say, filter and reduce) to compute the total value of the machines in the inventory array.

  ```js
  const inventory = [
    {type:   "machine", value: 5000},
    {type:   "machine", value:  650},
    {type:      "duck", value:   10},
    {type: "furniture", value: 1200},
    {type:   "machine", value:   77}
  ]

  let totalMachineValue = your_code

  console.log(totalMachineValue) // 5727
  ```

15. Sorted array

    The code for this exercise implements a wrapper for working with sorted arrays.
  Its constructor takes a comparison function that compares two elements and returns a number,
  negative if the first is less than the second, zero when they are equal,
  and positive otherwise (similar to what the sort method on arrays expects).

    Rewrite the code to use an ES6 class. Then, rewrite the loop to use the ES6 array method findIndex,
  which is like indexOf, but takes a function instead of an element as argument,
  and returns the index of the first element for which that function returns true (or returns -1 if no such element was found).
  For example [1, 2, 3].findIndex(x => x > 1) yields 1. Use arrow functions for all function expressions.

  ```js
  function SortedArray(compare) {
    this.compare = compare
    this.content = []
  }

  SortedArray.prototype.findPos = function(elt) {
    for (var i = 0; i < this.content.length; i++) {
      if (this.compare(elt, this.content[i]) < 0) break
    }
    return i
  }

  SortedArray.prototype.insert = function(elt) {
    this.content.splice(this.findPos(elt), 0, elt)
  }

  var sorted = new SortedArray(function(a, b) { return a - b })

  sorted.insert(5)
  sorted.insert(1)
  sorted.insert(2)
  sorted.insert(4)
  sorted.insert(3)
  console.log("array:", sorted.content)
  ```

  16. 5. Balancing parentheses.
    Write a function which validate that a supplied string is balanced.
    Example:

  ```js
  //  true
  isBalanced('(aaaa aaa aaa)', '()')
  isBalanced('(aaa aa[aa ]aa[a a]aaa', '[]')
  isBalanced('(aaa aa([aa() ])aa[a a]aa()a)', '()[]')

  //  false
  isBalanced('(aaaa (())aaa aaa))', '()')
  ```
  ---

  ## Tasks on DOM

1. Write a function which finds the red bordered node from "structure-1" in "structure-2" (set it the same border)
  eventually this function should be able to find any mirrored node specified in structure-1

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

1. Write a class called Point, which represents a point in two-dimensional space. A point has x and y properties, given
as arguments to its constructor. It also has a single method plus, which takes another point and returns the sum of the two points,
that is, a new point whose x is the sum of the x properties of the two original points, and whose y is the sum of their y properties.

```js
  console.log(new Point(1, 2).plus(new Point(2, 1))) // Point{x: 3, y: 3}
```

2. Speaker upgrade. Rewrite these two object types to use the class keyword, instead of direct prototype manipulation.
Speaker is a simple type that exposes a speak method which, when called, logs the given text along with the speaker's name.
Shouter is a subtype of Speaker which shouts its text and makes it uppercase.

```js
  function Speaker(name, verb) {
    this.name = name
    this.verb = verb || "says"
  }

  Speaker.prototype.speak = function(text) {
    console.log(this.name + " " + this.verb + " '" + text + "'")
  }

  function Shouter(name) {
    Speaker.call(this, name, "shouts")
  }

  Shouter.prototype = Object.create(Speaker.prototype)
  Shouter.prototype.speak = function(text) {
    Speaker.prototype.speak.call(this, text.toUpperCase())
  }

  new Shouter("Dr. Loudmouth").speak("hello there")
```

3. Getters. The way the verb property is set per instance rather than per class is kind of awkward.
Refactor the code to use a getter (get verb() { ... }) instead of an instance property.

4. Fake point. Use a single object literal to create an object that is indistinguishable from a Point instance, without calling the Point constructor.

```js
  class Point {
    YOUR_CODE_HERE
  }

  var fakePoint = YOUR_CODE_HERE
  console.log(fakePoint instanceof Point)
```
5. Singleton. Add a get method to the ids object, which returns the next id and increments its next counter. Use the short method syntax.

```js
  let ids = {
    next: 0
  }

  console.log(ids.get()) // 0
  console.log(ids.get()) // 1
```
6. Constant non-constance
Does the fact that account is constant mean that we can't update password? Why, or why not? And if not, how could we make it so that we can't?

```js
const account = {
  username: "marijn",
  password: "xyzzy"
}

account.password = "s3cret" // (*much* more secure)

console.log(account.password)
```

7. The detectCollision function searches through an array of rectangles and returns the first
rectangle that the given point is inside of. Use destructuring and a higher-order function to make this code cleaner.
You might want to use the new array method find, which takes a function as argument,
and returns the first element in the array (the element, not its index) for which the function returns true.

```js
  function detectCollision(objects, point) {
    for (let i = 0; i < objects.length; i++) {
      let object = objects[i]
      if (point.x >= object.x && point.x <= object.x + object.width &&
          point.y >= object.y && point.y <= object.y + object.height)
        return object
    }
  }

  const myObjects = [
    {x:  10, y: 20, width: 30, height: 30},
    {x: -40, y: 20, width: 30, height: 30},
    {x:   0, y:  0, width: 10, height:  5}
  ]
```
8. Avoiding disaster
This function uses destructuring for argument parsing. But it has a problem: it crashes when the caller passes an option object without an enable property. Since all options have defaults, we'd like to not crash in this case. Can you think of a clean way to fix this problem?

If you also want to allow not passing in an option object at all, how would you solve that?

```js
function go(options) {
  let {speed = 4, enable:
              { hyperdrive = false,
                frobnifier = true }} = options

  console.log("speed=", speed,
              "hyperdrive:", hyperdrive,
              "frobnifier:", frobnifier)
}

console.log(go({speed: 5}))
```

9. Default argument
It would be nice to be able to call our `lastIndexOf` function without providing the third argument, and have it default to starting at the end of the array. It would be even nicer if we could express this with an ES6 default argument value. Can we?

In which scope are default arguments evaluated? (Experiment to find out.)

```js
function lastIndexOf(arr, elt, start) {
  for (let i = start - 1; i >= 0; i--)
    if (arr[i] === elt) return i

  return -1
}

console.log(lastIndexOf([1, 2, 1, 2], 2))
```
