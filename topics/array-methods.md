# Array Methods

## Goals: 
- Learn the power of array manipulation
	- slice and splice
	- push, pop, shift, unshift
	- arguments (almost an array)
	- map, filter, reduce

**Assumes:** You already understand [basic JavaScript](new-to-js.md).

## Exercises:
You are given some membership data: Name, RSVP date, Member Since Date
```js
var data = [
    ['Alex','05/12/2015','07/28/2013'],
    ['Brett Chalupa','04/21/2015','03/13/2013'],
    ['Brian Cappello','04/20/2015','09/18/2013'],
    ['Cesar Carrasco','05/14/2015','08/14/2014'],
    ['Connor Finnerty','05/22/2015','05/12/2015'],
    ['Douglas Locklin','04/20/2015','01/30/2015'],
    ['Ian Metcalf','04/21/2015','01/19/2013'],
    ['Isaiah Keepin','04/20/2015','12/05/2013'],
    ['Ishmael Ahmed','04/22/2015','12/23/2013'],
    ['Jacob Dubois','04/20/2015','04/20/2015'],
    ['John brown','04/20/2015','01/17/2015'],
    ['Jonathan Hoguet','04/20/2015','04/28/2012'],
    ['Jordan Vartanian','04/28/2015','04/28/2015'],
    ['Joshua Burke','04/20/2015','08/27/2012'],
    ['Karlon Auger','04/21/2015','04/06/2015'],
    ['Matt Parrilla','04/20/2015','11/08/2013'],
    ['Mike Sullivan','04/26/2015','12/07/2013'],
    ['Mitchell Wulfman','05/20/2015','05/06/2014'],
    ['Nathan Sloma','04/20/2015','04/15/2013'],
    ['Nathaniel Jordan','04/20/2015','08/07/2014'],
    ['Pete Brown','04/21/2015','07/14/2012'],
    ['Rachel H','05/22/2015','02/22/2015'],
    ['Rob Friesel','04/25/2015','08/27/2013'],
    ['Ryan Patterson','05/17/2015','05/17/2015'],
    ['Sara Simon','04/20/2015','03/27/2015'],
    ['Tanya Lyn','04/20/2015','02/24/2015'],
    ['Tom Hadley','04/30/2015','11/30/2014'],
    ['Tyler Ortiz','04/27/2015','09/04/2013']
];
```

#### Exercise 1: What is the name and RSVP date for the 10 oldest members (by member since date)?

hint: consider using `map` to get away from arrays of arrays

what if you wanted to answer the same question but using only the first 15 items? last 15 items?

#### Exercise 2: How many members RSVP'd by year joined (Member Since Date)

hint: consider `reduce` when you need to reduce multiple items into a single item

#### Exercise 3: What percentage of RSVPs were within 1 week of the first announcement vs 1 week of the actual event?
