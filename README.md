# JavaScript Functions

### Statements, Expressions, & Declarations...

A computer program is a list of "_instructions_" to be "_executed_" by a computer.

In a programming language, these programming instructions are called `statements`.

A JavaScript program is a list of programming statements.


**Statement** = Roughly speaking, a statement specifies an action, can be defined as a line of code or a block of code. _Usually_ end with a semicolon `;`. (more on this later)

The purpose of other statements is to control the flow of the program, these are known as control statements such as `if` or `if-else` statements.

**Expression** = An expression is any valid unit of code that resolves to a single value.

**Declaration** = a declaration is a `statement` that describes an identifier, such as the name of a variable or a function. Declarations are important because they inform the compiler or interpreter what the identifying word means, and how the identified thing should be used.


The following is an example of an `if` statement:
```
var x;

if (y >= 0) {
    x = y;
} else {
    x = -y;
}
```
Expressions have an analog, the conditional operator. The above statements are equivalent to the following statement.
```
var x = (y >= 0 ? y : -y);
```
The code between the equals sign and the semicolon is an `expression`. The parentheses are not necessary, but I find the conditional operator easier to read if I put it in parenthesis.


---


### Ways To Write Functions...

**`Named Function` aka Function Declaration**
```
function myFirstFunction(parameter1, parameter2) {
    statement one;
    statement two;
    // comments about my code
    
    return;
}
```

**`Anonymous Function` aka Function Expression**
```
let mySecondFunction = function(parameter1, parameter2) {
    statement one;
    statement two;
    // comments about my code
    
    return;
};
```

**`Immediately Invoked Function Expression` aka IIFE**
```
let myThirdFunction = ( function() {
    statement one;
    statement two;
    // comments about my code
    
    return;
} () );
```
The final parenthesis **`()`** after the closing curly brace `}` of the code block tells the interpreter to call the function **immediately**.

The grouping operators are there to ensure the interpreter treats the function as an **expression**.

**Arrow Functions**

Arrow functions make it possible to write small **function expressions** in a less verbose fashion.

They have the following general form:

`let func = (arg1, arg2, ...argN) => expression`

This creates a function `func` that has arguments `arg1..argN`, evaluates the `expression` on the right side with their use and returns its result.

Examples:
```
let myFourthFunction = (x) => { 
    statement one;
    statement two;
    // comments about my code
    
    return;
};
```
Or
```
let myFourthFunction = (x) => x * x;
```

The `()` are optional if only a single argument is passed.



---


### Function Invocation

The code inside a JavaScript function will execute when "something" invokes it.

A JavaScript function can be invoked without being called (think IIFE's) 


---

### Miscellaneous 

* A **binding** is a variable in JavaScript and requires a name.
* An empty `return` statement or the absence of one, causes a function to return a value of `undefined`.
* Function **Parameters** vs Function **Arguments**???
  * Parameters are the values a function may accept, whereas Arguments are the values that are passed into a function. 
* callback functions
* lambda functions



