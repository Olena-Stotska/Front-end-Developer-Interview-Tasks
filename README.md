# Front-End Developer (task before first job)

I think everyone had issues with the first interview.
Every time there is a question in the head:
How to get ready?
Which task will be on interview?
Will I do that?
Panic... But don't worry :)
I picked up a few tasks for you, which will help you to get ready to interview.

## Tasks on Array

1. Write functions `some` & `every` which work as functions `Array.prototype.some` and `Array.prototype.every`

    ```js
    console.log(every([NaN, NaN, NaN], isNaN)) //true
    console.log(every([NaN, NaN, 4], isNaN)) //false
    console.log(some([NaN, 3, 4], isNaN)) //true
    console.log(some([2, 3, 4], isNaN)) //false
    ```
