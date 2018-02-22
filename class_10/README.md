# Introduction to jQuery

## What is jQuery?

jQuery is a cross-browser JavaScript library designed to simplify the client-side scripting of HTML.

It helps us out with:

- DOM traversal
- CSS manipulation through style attributes
- Event handling
- Animation
- And much more

## How to Use jQuery

- jQuery is available via CDN at code.jquery.com
- You can also download the library and serve it locally
- jQuery by itself is a library of functions. The team has also built additional tools that help us with a variety of things:
- jQuery UI: A UI tool that adds features such as additional easings, a datepicker, modals, effects, and more.
- jQuery Mobile: A mobile-optimized framework that allows you to create HTML5 mobile applications that look and act pretty real.

## jQuery Selectors

- The Sizzle selector engine wrapped into jQuery is a powerful tool to help us with manipulating DOM elements.
- The syntax is very similar to CSS:
```js
$("#myDiv > ul > li:first-child")

```

- Here the $ sign represents the jQuery library.


## jQuery Actions

- Actions almost always follow selectors.
- Actions are jQuery functions that perform an operation on the element(s) selected.
- The format is as follows:
```js
$("my-selector").action(options);
```

## DOM Manipulation

- The DOM manipulation functions in jQuery help you accomplish some pretty neat things.
- Here are a few common manipulations you will likely see:

On the fly CSS manipulations:
```js
$("my-selector").css("property", "value");
```

On the fly HTML manipulations:
```js
$("my-selector").html("New HTML inside here");
Altering CSS class attributes:

$("my-selector").addClass("new class");

$("my-selector").removeClass("class");

$("my-selector").toggleClass("class");
```

## Event Handling

- Event handling is done very smoothly with jQuery.
- There are a few different ways it can be performed, each having their use cases.
- Let's say we have a button and want to attach an event:

HTML
```html
<button id="my-button">Click Me!</button>
```
jQuery

- This is what I like to call the shortcut method.
- It has the limitation of not working when the DOM element doesn't already exist (think AJAX loading in dynamic content).

```js
$("#my-button").click(function() {
  //Your code here
});
```

- You can also bind events using .on
- This is also limited to elements that already exist, but it is a better approach.

```js
$("#my-button").on("click", function() {
  //Your code here
});
```
- Lastly, you can account for dynamic elements through binding the event to the document itself.
- This also happens to be the most performant if you look at benchmark tests.
```js
$(document).on("click", "#my-button", function() {
  //Your code here
});
```
- Here is a list of the most common events you are likely to see:
  - Click
  - Keyup
  - Keydown
  - Mouseenter
  - Mouseleave
  - Dblclick
  - Change

## Homework

## DOM Manipulation Exercise: Shakespeare's Plays

- Download the starter code files.
- Add a class of special to all of the li elements at the second level of the nested list.
- Add a class of year to all of the table cells in the third column of a table.
- Hint: Take a look at how many columns are in each table.
- Add the class of special to the first table row that has the word Tragedy in it.
- Challenge: Select all of the list items li containing a link a. Add the class afterlink to the sibling list items that follow the ones selected.
- Challenge: Add the class tragedy to the closest ancestor ul of any .pdf link.
