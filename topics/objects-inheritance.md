# Objects and Inheritance

##Goals: 
- Learn the power of objects and inheritance 
	- new, {}, Object.create
	- constructor functions
	- prototypal inheritance, mixin pattern

**Assumes:** You already understand [basic JavaScript](new-to-js.md). 

## Exercises: 

I suggest you run these using a JavaScript REPL such as [repl.it](https://repl.it/languages/javascript) or [node](https://nodejs.org/).

Use the [MDN JavaScript Documentation](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference) for help as you go!

Each exercise ends with a call to `assert()`. That function will print `correct!` to the console if the exercise is successful. 

### Exercise 1: Create an object that has a property using three different techniques.

The techniques are: the object literal, `new`, and `Object.create`.

```javascript
function assert(val, name) { if (val) return console.log(name + ' is correct!'); console.log(name + ' is incorrect.'); }

// Do something below to create three objects, each with a property named 'color'.
var object1 = undefined;
var object2 = undefined;
var object3 = undefined;

assert(object1.color === 'green', 'Exercise 1 object1');
assert(object2.color === 'green', 'Exercise 1 object2');
assert(object3.color === 'green', 'Exercise 1 object3');
```

### Exercise 2: Reimplement the `new` operator.

In the following code, we use `new` to inherit a property. Reimplement this code without using `new`. Take a look at the documentation of [Object.create](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object/create) for help.

```javascript
function assert(val, name) { if (val) return console.log(name + ' is correct!'); console.log(name + ' is incorrect.'); }

var Foo = function() {}
Foo.prototype.color = 'green';
var object1 = new Foo();

// The above code creates a new object that inherits the `color` property
// Change the following line to create another object that inherits that
// property without using `new`.
var object2 = undefined;

assert(object2.color === 'green', 'Exercise 2');
```

Hint: the `new` operator does three things. We only need the first one in this exercise.

1. Creates a new object with the internal prototype set to the `prototype` property of the constructor function.
2. Calls the constructor function, binding `this` to the new object.
3. Returns the new object or the return value of the constructor function if one exists.

### Exercise 3: Use prototype inheritance to change the value of a group of objects.

In the following code we create two objects which inherit the property `color`. Add only one line of code **after the objects have been created** which changes the color of both objects to `'blue'`;

```javascript
function assert(val, name) { if (val) return console.log(name + ' is correct!'); console.log(name + ' is incorrect.'); }

var Foo = function() {};
Foo.prototype.color = 'yellow';
var object1 = new Foo();
var object2 = new Foo();

// At this point both objects have the `color` property set to `yellow`.
// Add only one line of code below here to change both of them to blue.

assert(object1.color === 'blue', 'Exercise 3 object1');
assert(object2.color === 'blue', 'Exercise 3 object2');
```

### Exercise 4: Override prototype inheritance in an object.

In the following code, we use prototypal inheritance to give two objects the property `color` which equals `'yellow'`. By adding only one line of code **after the objects have been created**, make it so that one object has the color `'green'` and the other color remains `'red'`. 

```javascript
function assert(val, name) { if (val) return console.log(name + ' is correct!'); console.log(name + ' is incorrect.'); }

var Foo = function() {};
Foo.prototype.color = 'yellow';
var object1 = new Foo();
var object2 = new Foo();

// At this point both objects have the `color` property set to `yellow`.
// Add only one line of code below here to change object1 to blue.

assert(object1.color === 'blue', 'Exercise 4 object1');
assert(object2.color === 'yellow', 'Exercise 4 object2');
```

### Exercise 5: Use the mixin pattern to inherit properties from multiple sources.

Create two constructor functions, `Flying` and `Singing`. Create a new object `bird` that inherits from both of these functions. `Flying` should add the function `fly()` and `Singing` should add the function `sing()`. 

The mixin pattern allows a form of inheritence without using `prototype` or `new` and as a result can sometimes be much easier to understand, but it is not persistent like prototypal inheritance.

```javascript
function assert(val, name) { if (val) return console.log(name + ' is correct!'); console.log(name + ' is incorrect.'); }

function Flying(thing) {
    thing.fly = function() {
        console.log('flap flap!');
        return true;
    }
}

function Singing(thing) {
    thing.sing = function() {
        console.log('tweet tweet!');
        return true;
    }
}

var bird = {};

// Use the constructor functions above as mixins to add `fly` and `sing`
// to the `bird` object without using `new`.

assert(bird.fly(), 'Exercise 5 flying');
assert(bird.sing(), 'Exercise 5 singing');
```
