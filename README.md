Teaching Programming
================
Using Javascript as an Example

**This is not for students to work with directly, but for those interested in instruction.**

# Introduction

Learning to code is hard and it shouldn’t be.  *I agree with Bret Victor that this is in great part due to programming languages being poorly designed.  Ease of learning should be a core design consideration in creation of programming languages, and programmer should stop finding it acceptable for things to be otherwise. (Read more about this here: [http://worrydream.com/LearnableProgramming/](http://worrydream.com/LearnableProgramming/) )*

Unfortunately, I'm not introducing a new programming system, but I do have an interest immediately in helping those who are interested in programming.  

I belive in a direct person-to-person involvement in education; I don’t think we should be indifferent to people’s failures in learning, since a failure in these matters often makes it harder to make another attempt.  We should not leave those who want to learn stranded.

The following stages are intended to be repeated multiple times, and require the guidance of someone who is already familiar with the technology you are trying to learn.  Therefore, this document is for those who want to teach as much (if not more) than those who want to learn.  Both teacher and student should be familiar with this document so that all parties understand the process involved.

# Work for the Teacher

## Analysis of Technology

This will require some homework for the teacher.  The idea is to evaluate the technologies you will be teaching so you can fit the different components to the following sections.  

I'm going to talk about this more in depth in the section titles Programming Ontology


## Analysis of the Student

Discover how much the student already know?

# Work for the Student

## Environment Setup

This sucks.  Fortunately it isn’t so hard with Javascript, since you already have a browser.

## Grammar

Before we learn to write we learn to read.  Why is this different with programming?  In English, when we read we proceed from the top of the page to the bottom and from left to right.  (Of course, sometimes footnotes or end notes are used, and this can be an helpful thing for programmers to relate to.)

### Statements and Expressions

### Values, Labels, Operators

### Left Hand and Right Hand

### Functions

### Comments

### Composing Expressions from Other Expressions

### Program Flow, or How to Move from One Line to Another

One can't always assume that the next line of code that will be run is on the following line.

#### `if` Statements

#### `for` and `while` Statements

#### `switch` Statements

### Resources

[You Don't Know JS on Statements](https://github.com/getify/You-Dont-Know-JS/blob/master/up%20&%20going/ch1.md)

## Vocabulary Study

Suggest that the student learning vocabulary involved in the technologies they want to learn.  Reading articles, watching tutorials and looking at questions/answers (on stackoverflow), even with little comprehension can help provide a realistic view of ignorance on a subject, and help with encountering new terms.

*Programming Terminology Resources:*

* [http://www.codecademy.com/glossary/javascript](http://www.codecademy.com/glossary/javascript)

* [https://developer.mozilla.org/en-US/docs/Glossary](https://developer.mozilla.org/en-US/docs/Glossary)

## Iterate Over These Following Steps:

* Try emphasizing a type on each iteration. 

    * In early iterations start with simple types

        * text, number, truth values

        * It’s ok to do all three of these at once, but emphaze only one at a time

    * After simple types work with aggreate types

        * lists, generic

    * After aggregate types work with program blocks

        * functions

    * After all of these, try going through using combinations of these

    * After this, start adding more application layers, but one at a time.

        * For each application layer you add, the entire process may have to be repeated, starting with basics of that layer.

* Practice putting/getting values with that particular type.

* Practice manipulations on that type

* Practice control flow with that type

    * Understand truth values of a type

* Go Over some Common tasks With a type

* If you have covered basic types (text, number, truth value)

    * Work with built in features

### Types (Conceptually)

Text (String, char)

Number (int, float, double)

Truth Value (Boolean)

Algorithm (Function)

Lists (Array)

Generic (Object)

### Putting and Getting Values

A level/layer/part of a software system is defined by a programming interface for putting and getting values.  

Here are some different levels of a system programmers might interact with

* Memory: data we put in local variable are manipulating direcly in our program.  This is the most essential layer for programming.

    * ```var x = 2; x = x * 2; console.log(x);```

* Network (we can put and get values from the network)

    * HTTP request (‘web’ request)

    * TCP/UDP

* File System

* Other programs (via an api used in our program or through the network)

    * Database (on current machine or through network)

    * Browser (*e.g.*, Document Object Model, or DOM)

    * Service on network (Facebook)

* User (we can prompt user for input)

*e.g.*:
```javascript
var x = 12;

console.log(x);

(function(x) {

	console.log(x);

})(12);

var x = [1,2,3];

console.log(x[0]);
```

### Simple Data Manipulation

+, -, /, *, %  

()

||, && 

++x, x++, +=

### Control of Program Flow

if

else 

for

can probably avoid:

while

do...while

switch

### Common Tasks

* Find text in a string

* Evaluate a mathematical expression

* Traverse an array (in order to find something)

### Extra: Built In Features For Types / API Features

*e.g.*, array.prototype functions

### Extra: Grammars from Convention

*e.g.*, fluent

### Extra: Patterns

*e.g.*, Closure, module pattern

## Advanced Topics

These topics don’t need to be covered until the student has relative autonomy.

### Software Design Principles

SOLID

<table>
  <tr>
    <td>Initial</td>
    <td>Stands for
(acronym)</td>
    <td>Concept</td>
  </tr>
  <tr>
    <td>S</td>
    <td>SRP [4]</td>
    <td>Single responsibility principle
a class should have only a single responsibility (i.e. only one potential change in the software's specification should be able to affect the specification of the class)</td>
  </tr>
  <tr>
    <td>O</td>
    <td>OCP [5]</td>
    <td>Open/closed principle
"software entities … should be open for extension, but closed for modification."</td>
  </tr>
  <tr>
    <td>L</td>
    <td>LSP [6]</td>
    <td>Liskov substitution principle
“objects in a program should be replaceable with instances of their subtypes without altering the correctness of that program.” See also design by contract.</td>
  </tr>
  <tr>
    <td>I</td>
    <td>ISP [7]</td>
    <td>Interface segregation principle
“many client-specific interfaces are better than one general-purpose interface.”[8]</td>
  </tr>
  <tr>
    <td>D</td>
    <td>DIP [9]</td>
    <td>Dependency inversion principle
one should “Depend upon Abstractions. Do not depend upon concretions.”[8]
Dependency injection is one method of following this principle.</td>
  </tr>
</table>


DRY (Don’t Repeat Yourself)

If you do something more than once, consider writing a function.

# Elements of Programming (Ontology)

This section is rather philosophical, but perhaps most fruitful for teachers.  I should provide a warrant for this section, but I think that after investing some time in it the importance will show itself.

## Layer (this term may not be the most suitable)

*A layer is basically anything that you can put some value into, or get some value out of.*

### Overview

Programming languages abstract many different systems into a single interface.  Software developers most typically work with conceptual layers (objects, classes, &c), however, it is also common that one would write code against a system that interfaces with another service or even hardware.

Working with many layers in an application is almost always necessary, and these layers presents different metaphores and terminology.  Often these different systems have conflicting metaphores and produce equivocations on terms if they aren't kept distinct.  Developing an intuitive understanding of different layers of a system and how each are brought to stand in the same environment can be very helpful for overcoming a lot of confusion on the part of the student.

New developers can help themselves by understanding that they will need to take these different metaphores and potentially wresle them into a common metaphore.  A good example of how systems are made to work together is given with a *nix command prompt.  When running commands together with pipes (`|`), every command passes its results to the next command as text.  In this way there is a consistant expectation for what every console application can work with.

### Examples of Layers

	var x = {}; //stores in local 'memory'/context layer
	
	x.method = function(){}; //this is a conceptual layer we are making on our object
	
	$http.post('www.example.com/v1/restapi'); //puts to the network
	
	db.table.save({data: "data"}); //puts to the database network interface layer

Frequently new programmers don't understand the nature of the conceptual systems they are interfacing with, and how these in turn interface with other systems and ultimately with hardware.  While it isn't necessary to understand everything that is going on, it will help to teach the developer to think in terms of parts of a system operating with each other.
