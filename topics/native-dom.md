# Native Document Object Model

##Goals: 
- Introduce native JavaScript for manipulating the Document Object Model
	- createElement
	- appendChild
	- getElementById
	- getElementsByTagName
	- getElementsByClassName
	- querySelector
	- querySelectorAll
	- manipulating attributes
	- manipulating classes

**Assumes:** You already understand [basic JavaScript](new-to-js.md). 

## Exercises: 

### Exercise 1: Add some `h1` text to a page's DOM

Given a simple page, for example the following,

```html
<html>
  <body>
  </body>
</html
```

...create and append an `h1` element, like `<h1>hello world</h1>`, to the body of the page.

Hint: A web-based development tool like [codepen](http://codepen.io/) or [jsfiddle](http://jsfiddle.net/) can be very useful to play with these concepts.

### Exercise 2: Query and set the style property of a DOM element by ID

Given the following html page,

```html
<html>
  <body>
    <div>MY LOGO</div>
    <div id="site-title">My Website</div>
    <div id="site-tagline">The best site ever.</div>
  </body>
</html>
```

...modify the style of the site title (the element with the text "My Website" and the ID `site-title`) to render it in the color blue. **Only one line should become blue!**

### Exercise 3: Query and set the CSS class of a DOM element by selector

Given the following html page,

```html
<html>
  <head>
    <style type="text/css">
      .highlighted { background-color: yellow; }
    </style>
  </head>
  <body>
    <div class="heading-text primary">My Website</div>
    <div class="heading-text secondary">The best site ever.</div>
    <div class="body-text primary">I love web development.</div>
    <div class="body-text secondary">It's magical.</div>
  </body>
</html>
```

...find the page element that has both the class `heading-text` and the class `secondary` and add the class `highlighted`. This will cause that line to become highlighted in yellow. **Only one line should be highlighted!**

