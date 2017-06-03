# Callbacks and Promises

## Goals: 
- Learn the power of promises
	- callback hell
	- promises
	- .then
	- .all

**Assumes:** You already understand [basic JavaScript](new-to-js.md).

* Jake Archibald wrote a [great article](http://www.html5rocks.com/en/tutorials/es6/promises/) for HTML5 Rocks about native JavaScript Promises. Read the whole thing when you get a chance.
* [Promise API Reference from HTML5 Rocks](http://www.html5rocks.com/en/tutorials/es6/promises/#toc-api)

## Exercises:

### Exercise 1. [Print Eat, Sleep, Work in that order without using Promises (jsfiddle)](http://jsfiddle.net/donniec/k65ttyvn/2/)
The functions `eat()`, `sleep()`, and `work()` each return asynchonously after a different random interval. Consequently, the code will not always print the desired, ordered result. Run the fiddle a few times and see for yourself.

Each of these functions can take a [callback](https://en.wikipedia.org/wiki/Callback_(computer_programming)) function that will be called when the function is finished executing.
Use callbacks to fix the code.

### Exercise 2.  [Use Promises to fix Callback Hell (jsfiddle)](http://jsfiddle.net/sfwxzybs/4/)
What if you wanted to add another function, `bathe()`, or to change the order of output? Callback Hell can quickly become tedious. Thankfully, there is a better way: `Promises` are a way to reason about asynchrony in a synchronous way.  
A `Promise` is constructed with a callback function that takes two parameters, `resolve` and `reject`. When the `Promise` finishes doing whatever/whenever, it calls `resolve()` (or `reject()` if an error occurred). Functions that return `Promises` are _chained_ (rather than _nested_) by wrapping them in a `then()` function (see the documentation for how to use `then()`).

`eat()`, `sleep()`, and `work()` now return `Promises`. Chain them in order to ensure order.

Hint: Each function will return a `Promise` so that the next _composed_ function is called once the `Promise` is _resolved_.

### Exercise 3. [blah, blah, blah, ..., WEEKEND! (jsfiddle)] (http://jsfiddle.net/qnquxh16/2/)
Use `.map()` to create an array of `Promises` for every weekday, Monday through Friday. Print out the day, and when those are done, print `WEEKEND!`. The order of the days doesn't matter at this point.

Hint: `Promise.all()` takes an array of `Promises` and returns its own `Promise`, which is _resolved_ when all the `Promises` in the array are resolved, though it doesn't ensure order.

### Exercise 4. [Print out the Days of the Week in Order (jsfiddle)] (http://jsfiddle.net/vgd41yvm/7/)
One of the great things about `Promises` is that they can be essentially _resolved before_ they're used. If you create a chain of `.then()` calls, each one returning a `Promise` to the next, if a `Promise` in the middle of that chain is resolved ahead of time, the order of composed functions is still preserved, and we won't have to wait on the already-resovled promise.

Use `.reduce()` to create a single chain of `Promises` that will print out the days of the week in order. When those are done, print `WEEKEND!`.

### Bonus Exercise 5. [Print out the Days of the Week in Order w/ Generators (jsfiddle)] (http://jsfiddle.net/4uog8kor/2/)
Using ES6 Generators and Promises, we can ensure order without using reduce.

Use the `spawn()` helper function to print out the days of the week in order. When those are done, print `WEEKEND!`.

In ES7, the helper function won't be necessary and will be replaced with `async` functions.
