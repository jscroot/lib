# Element Functions

## Introduction

This module provides a collection of JavaScript utility functions to simplify common DOM manipulations, event handling, and dynamic content management.

## Installation

Simply include the JavaScript file in your project or import the functions as an ES module:

```javascript
import { onClick, onClicks, container, setValue, getValue, renderHTML, addJS, addCSS } from 'https://cdn.jsdelivr.net/gh/jscroot/lib@0.2.3/element.js';
```

## Functions and Usage

### DOM Selection

#### `container(id)`

Gets an element by its ID.

```javascript
const element = container('myElement');
```

### Event Handling

#### `onClick(id, actionFunction)`

Adds a click event listener to an element by ID.

**Example without arguments:**

```javascript
function handleClick() {
    console.log("Button clicked!");
}

onClick('myButton', handleClick);
```

**Example with arguments:**

```javascript
function handleClickWithArgs(target) {
    console.log("Button clicked!", target.id);
}

onClick('myButton', handleClickWithArgs);
```

#### `onClicks(className, actionFunction)`

Adds a click event listener to all elements with the specified class.

**Example without arguments:**

```javascript
function handleMultipleClicks() {
    console.log("An element was clicked!");
}

onClicks('myClass', handleMultipleClicks);
```

**Example with arguments:**

```javascript
function handleMultipleClicksWithArgs(element) {
    console.log("Clicked element:", element.className);
}

onClicks('myClass', handleMultipleClicksWithArgs);
```

#### `onChange(id, actionFunction)`

Adds a change event listener to an element.

```javascript
function handleChange(element) {
    console.log("Input changed:", element.value);
}

onChange('myInput', handleChange);
```

#### `onInput(id, actionFunction)`

Adds an input event listener to an element.

```javascript
function handleInput(element) {
    console.log("Input value:", element.value);
}

onInput('myInput', handleInput);
```

### DOM Manipulation

#### `setValue(id, valueContent)`

Sets the value of an input field.

```javascript
setValue('myInput', 'New Value');
```

#### `getValue(id)`

Gets the value of an input field.

```javascript
const value = getValue('myInput');
console.log(value);
```

#### `setInner(id, content)`

Sets the inner HTML of an element.

```javascript
setInner('myDiv', '<p>Hello World</p>');
```

#### `setInnerText(id, content)`

Sets the inner text of an element.

```javascript
setInnerText('myDiv', 'Hello World');
```

### Visibility and Styling

#### `show(id)`

Displays an element by setting `display: block`.

```javascript
show('myDiv');
```

#### `hide(id)`

Hides an element by setting `display: none`.

```javascript
hide('myDiv');
```

### Dynamic Content Loading

#### `renderHTML(id, urlHTML, callback = null)`

Loads external HTML content into an element.

```javascript
function afterContentLoad() {
    console.log('Content loaded successfully');
}

renderHTML('content', 'content/home.html', afterContentLoad);
```

### Script and CSS Management

#### `addJSInHead(src)`

Dynamically adds a JavaScript file to the document head.

```javascript
await addJSInHead('https://example.com/script.js');
```

#### `addCSSInHead(href)`

Dynamically adds a CSS file to the document head.

```javascript
await addCSSInHead('https://example.com/styles.css');
```

#### `isCSSLoaded(href)`

Checks if a CSS file is already loaded.

```javascript
if (isCSSLoaded('styles.css')) {
    console.log('CSS is already loaded');
}
```

#### `isJSLoaded(src)`

Checks if a JavaScript file is already loaded.

```javascript
if (isJSLoaded('script.js')) {
    console.log('JS is already loaded');
}
```

#### `addJS(src)`

Adds a JavaScript file to the document only if it is not already loaded.

```javascript
await addJS('https://example.com/script.js');
```

#### `addCSS(href)`

Adds a CSS file to the document only if it is not already loaded.

```javascript
await addCSS('https://example.com/styles.css');
```

## Conclusion

This utility module simplifies DOM interaction and event handling, making it easier to manage dynamic web applications. Use these functions to streamline your JavaScript code!

