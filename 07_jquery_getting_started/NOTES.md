# jQuery: Getting Started

Using vanilla JS in the DOM is often far too verbose and complicated.

jQuery gives us a very simple way of interacting with the DOM without
the pain and complexety of the DOM.

jQuery also solves a number of cross browser compatability issues for us.
This is still applicable in modern web development.

## Anatomy of a jQuery Command

`$` is a shortcut for jQuery. You could replace it with the `jQuery` variable.
In the vast majority of cases you will use the `$` though.

The jQuery command is a function.

Hello World example:

```javascript
$(function () {
    console.log("Hello World");
});
```

The jQuery selector returns an array of matching items.
In technical terms this is called a _wrapped set_.

If there is no match for a jQuery selector you return an empty array.

Many jQuery functions are a combination getter and setter.

jQuery functions will work against an entire wrapped set.

## Finding Parts of a Page

jQuery primarily uses CSS3 selectors.

- **ID:** Unique to a single element. Identified by a `#` prefix.
- **Class:** - Applied to one or more elements. Identified by a `.` prefix.
- **Psudeo-Class:** - An element in a particular state. Identified by a `:` prefix.

You can pass a HTML string into the jQuery selector to create a new
element in memory.

You can also pass raw DOM elements into a jQuery selector to convert
them into a wrapped set.

## Adding Style and Effects

The `.attr()` jQuery function allows us to maniplulate element attributes.

The `.css()` function is preferred when dealing specifically with the
HTML `style` attribute.

With the `.css()` function we use camelCase rather than hyphenated-syntax
for the names of CSS rules.

We can use `.addClass()` or `.removeClass()` to add and remove classes.

To hide an element use the `.hide()` function. The `.show()` function
provides the alternate. To change to the opposite state use the
`.toggle()` function.

For additional effect we can use `.fadeOut()` and `.fadeIn()`.

## Events

Use the document ready event to check if the page is fully loaded.

Use the `.on()` function to handle events.

Use the `.off()` function to remove a listner from an event.

_We appear to be using the observer pattern here_.

Use the `.one()` function to make sure an event is only handled once.

Use the `.click()` function for specific handling of the click event.

## Chaining

jQuery allows us to chain functions with dot notation to avoid the
inefficiency of re-selecting the elements for every manipulation.