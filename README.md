# Front-end Developer Interview Tasks

This file contains tasks Front-End interview.

I hope, these tasks help fresh developers prepare to interview and for interviewer find potential candidates.

## Tasks on Array

1. Write functions `some` & `every` which work as functions `Array.prototype.some` and `Array.prototype.every`

    ```js
    console.log(every([NaN, NaN, NaN], isNaN)) //true
    console.log(every([NaN, NaN, 4], isNaN)) //false
    console.log(some([NaN, 3, 4], isNaN)) //true
    console.log(some([2, 3, 4], isNaN)) //false
    ```

2.
