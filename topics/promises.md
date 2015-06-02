# Callbacks and Promises

##Goals: 
- Learn the power of promises
	- callback hell
	- promises
	- .then
	- .all

**Assumes:** You already understand [basic JavaScript](new-to-js.md). 

* Jake Archibald wrote a great article for HTML5 Rocks about native JavaScript Promises. Read the whole thing when you get a chance.
* [Promise API Reference from HTML5 Rocks](http://www.html5rocks.com/en/tutorials/es6/promises/#toc-api)

## Exercises:

### Exercise 1. [Print Eat, Sleep, Work in that order](http://jsfiddle.net/donniec/k65ttyvn/)
The functions `eat()`, `sleep()`, and `work()` each return asynchonously after a different random interval. Consequently, the code will not always print the desired, ordered result. Run the fiddle a few times and see for yourself.

Each of these functions can take a callback function that will be called when the function is finished executing.  
Use callbacks to fix the code.

### Exercise 2.  [Use Promises to fix Callback Hell](http://jsfiddle.net/donniec/sfwxzybs/1/)
What if you wanted to add another function, `bathe()`, or to change the order of output? Callback Hell can quickly become tedious. Thankfully, there is a better way: `Promises` are a way to reason about asynchony in a synchronous way.  
A `Promise` is constructed with a callback function that takes two parameters, `resolve` and `reject`. When the `Promise` finishes doing whatever/whenever, it calls `resolve()` (or `reject()` if an error occurred). Functions that can handle promises are _composed_ (rather than _nested_).

Modify `eat()`, `sleep()`, and `work()` to use `Promises` instead of nested callbacks.

Hint: Each function should return a `Promise` so that the next _composed_ function is called once the `Promise` is _resolved_.

### Exercise 3. [blah, blah, blah, WEEKEND!] (http://jsfiddle.net/donniec/qnquxh16/)
Use `.map()` to create an array of `Promises` for every weekday, Monday through Friday. Print out the day, and when those are done, print `WEEKEND!`. 

Hint: `Promise.all()` is like `.then()` but it takes an array of `Promises` and it returns its own `Promise`, which is _resolved_ when all the `Promises` in the array are resolved, regardless of order.

### Exercise 4. [Print out the Days of the Week in Order] (http://jsfiddle.net/donniec/vgd41yvm/1/)
One of the great things about `Promises` is that they can be essentially _resolved before_ they're used. If you create a chain of `.then()` calls, each one returning a `Promise` to the next, if a `Promise` in the middle of that chain is resolved ahead of time, the order of composed functions is still preserved, and we won't have to wait on the already-resovled promise.

Use `.reduce()` to create a single chain of `Promises` that will print out the days of the week in order. When those are done, print `WEEKEND!`.
