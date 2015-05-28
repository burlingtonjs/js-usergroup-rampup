# Objects and Inheritance

##Goals: 
- Learn the power of objects and inheritance 
	- new, {}, Object.create
	- constructor functions
	- prototypal inheritance

**Assumes:** You already understand [basic JavaScript](new-to-js.md). 

## Exercises: 

### Exercise 1: Create an object that has a property using three different techniques.

Hint: `new`, `Object.create`, and the object literal.

### Exercise 2: Reimplement the `new` operator.

In the following code, we use `new` to inherit a property. Reimplement this code without using `new`.
```javascript
var Foo = function() { this.name = 'an object'; }
Foo.prototype.color = 'green';
var myFoo = new Foo();

myFoo.name === 'an object'; // returns true
myFoo.color === 'green'; // returns true
```

Hint: the `new` operator does three things:

1. Creates a new object with the internal prototype set to the `prototype` property of the constructor function.
2. Calls the constructor function, binding `this` to the new object.
3. Returns the new object or the return value of the constructor function if one exists.

### Exercise 3: Use prototype inheritance to change the value of a group of objects.

In the following code we create two objects, `myFooOne` and `myFooTwo`, which inherit the property `color`. Add only one line of code **after the objects have been created** which changes the color of both objects to `'blue'`;
```javascript
var Foo = function() {};
Foo.prototype.color = 'yellow';
var myFooOne = new Foo();
var myFooTwo = new Foo();

myFooOne.color === 'yellow'; // returns true
myFooTwo.color === 'yellow'; // returns true
```

### Exercise 4: Override prototype inheritance in an object.

In the following code, we use prototypal inheritance to give two objects the property `color` which equals `'red'`. By adding only one line of code **after the objects have been created**, make it so that one object has the color `'green'` and the other color remains `'red'`. 
```javascript
var Foo = function() {};
Foo.prototype.color = 'red';
var myFooOne = new Foo();
var myFooTwo = new Foo();

myFooOne.color === 'red'; // returns true
myFooTwo.color === 'red'; // returns true
```
