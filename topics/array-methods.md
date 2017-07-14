# Array Methods

### Get Started
Reference Url: [https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array)

When working in the console, note that `Shift + Enter` will allow you to write your code on multiple lines. Copy this code and paste it in your console.

```js
var names =
    ['Cesar', 'David', 'Alex','Evelyn', 'Dora', 'Fred', 'Betty', 'Annie'];
```
### Warm-ups
####  Using splice (mutator)
- Add 'Ava' to the beginning of the array
- Remove 'Fred' from the array and insert 'Frank'
- Insert 'Daryl' twice, right next to 'David'

#### More mutators
- Use `pop` to remove the last person from the array
- Use `push` to add that person back
-	Use `shift` to remove the first person from the array
- Use `unshift` to add that person back
- Use `reverse` to flip the order of the array.
- Use `sort` to alphabetize the list

#### Functional methods (non-mutator)
- Use `map` to capitalize all of the names.
- Use `filter` to find a list of names that start with the letter 'A'.
- Use `reduce` to find the longest name.
- With `map` and `slice`, get a list of the first letters of each name.


#### Exercises
You may need to incorporate other methods found on the [MDN page](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array) to complete these exercises.  Consider using method chaining where appropriate.

1. Add an exclamation point (!) to the end of everyone's name (from Warm-ups), then `console.log` a boolean to confirm that all the names in the array end in an exclamation point.

```js
var people =
    [{'name':'Cesar', 'age':53},
      {'name':'Alex', 'age':29},
      {'name':'Evelyn', 'age':40},
      {'name':'Dora', 'age':80},
      {'name':'Fred', 'age':21},
      {'name':'Betty', 'age':36},
      {'name':'Annie', 'age':48}
    ];
```

2. Iterate over the `people` above and `console.log` out the people in order of their age, highest to lowest.

3. Use `reduce` to add up all of the ages of the `people` and `console.log` the total.
