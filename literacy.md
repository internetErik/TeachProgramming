# JavaScript Literacy

Examples of JavaScript code for the purpose of learning some syntax, and become literate in the language

## Heuristics

These heuristics are intended to help you read code actively by asking questions about it.

### Statements, Expressions and Comments

#### Overview

*Statements* are code that perform and actions (*i.e.,* control flow, assignment, etc), but doesn't produce a value

*Expressions* are any piece of code that, when executed, becomes a value.

*Comments* are non-executable portions of programs. These are often used for documentation, or visually signaling something. The existence of comments can impact performance.

#### Statements

*Allocation or Creating Variables*

These statements in some way implicitely allocate memory, even though (in JavaScript) memory is managed by the environment and not by the programmer.

```javascript
// simple allocating
var a; // hoisted
let b; // not hoisted, local scope
const c; // local scope, cannot be reassigned

// multiple allocations
var a, b, c;
let d, e, f;
const g, h, i;

// multiple allocations can happen on new lines
var someName,
    anotherName;
```

*Note:* Another way to create a variable that is scoped to a single area is to use a function

```javascript
// these all both create and execute a function
(function(a) { console.log(a); })(10); // "dog balls" - Crockford
(function(a) { console.log(a); }(5));
((a) => console.log(a))(8);
((a) => console.log(a)(12)); // X this doesn't work
```

*Assignment*

```
// simple assignment
var a = 100; // hoisted
let b = 'This is a string'; // not hoisted, local scope
const c = { a: 'test' }; // local scope, cannot be reassigned
const ar = ['this', 'is', 'an', 'array'];

// multiple allocations
var a, b = 10, c;
let d = `A template string ${b}`, e, f;
const g = 10.10, h, i = 'a string';

// multiple allocations can happen on new lines
var someName = 'One value here',
    anotherName = 'Another value here';
```


### Where was this Defined?

#### I Defined It

**How can I tell?**


#### It is a Part of the JavaScript Language

**How can I tell?**


#### It is Defined by the Runtime Environment

**How can I tell?**


#### It is Defined by a Libraries or Frameworks

**How can I tell?**


### `this` (Advanced)


## Reading

### Sequential Code

```javascript
var x = 1;
console.log(x);

x = x + 1;
console.log(x);
```

```javascript
var flag = true;

if(flag) {
  console.log("Flag is on");
}
else {
  console.log("Flag is off");
}

flag = false;

if(flag) {
  console.log("Flag is on");
}
else {
  console.log("Flag is off");
}
```

```
```

### Non-Sequential Code

