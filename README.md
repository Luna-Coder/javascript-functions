# JavaScript Functions

## Statements, Expressions, & Declarations...

### JavaScript `statements`

- Roughly speaking, a `statement` specifies an action. It can be defined as a line of code or a block of code. _Usually_ ends with a semicolon `;`. (more on this later).

- A computer program is a list of "_instructions_" to be "_executed_" by a computer.

- In a programming language, these programming instructions are called `statements`.

- A JavaScript program is a list of programming statements.

- The purpose of other statements is to control the flow of the program, these are known as `control statements` such as `if` or `if-else` statements. Loops are also `statements`.
  

### JavaScript `expressions`

- An `expression` is any valid unit of code that resolves to a single value.


### JavaScript `declarations`

- A `declaration` is a `statement` that describes an identifier, such as the name of a `variable` or a `function`.

- JavaScript `declarations` are important because they inform the compiler or interpreter what the identifying word means, and how the identified thing should be used.

The following is an example of an `if-statement`:
```js
let x;

if (y >= 0) {
    x = y;
} else {
    x = -y;
}
```

- JavaScript `expressions` have an analog, the conditional (ternary) operator `(? :)`. The above `statements` are equivalent to the following `statement`.
```js
let x = (y >= 0 ? y : -y);
```
- The code between the assignment operator (`=`) and the semicolon (`;`) is an `expression`.

- The parentheses `()` are not necessary, but I find the conditional (ternay) operator `(? :)` easier to read if I put it in parenthesis.


---


## Ways To Write Functions...

### `Named Functions` aka `Function Declarations`
```js
function myFirstFunction(parameter1, parameter2) {
    statement one;
    statement two;
    // comments about my code
    
    return ___;
}
```

### `Anonymous Functions` aka `Function Expressions`
```js
let mySecondFunction = function(parameter1, parameter2) {
    statement one;
    statement two;
    // comments about my code
    
    return ___;
};
```

### `Immediately Invoked Function Expressions` aka `IIFEs`
```js
let myThirdFunction = ( function() {
    statement one;
    statement two;
    // comments about my code
    
    return ___;
} () );
```
- The final parenthesis `()` after the closing curly brace `}` of the code block tells the interpreter to call the function **<ins>immediately</ins>**.

- The grouping operators are there to ensure the interpreter treats the function as an `expression`.



### ES6 Function Shorthand aka `Arrow Functions`

- Arrow functions make it possible to write small `function expressions` in a less verbose fashion.

- They have the following general form:

```js
let func = (arg1, arg2, ...argN) => expression;
```

- This creates a function `func` that has arguments `arg1..argN`, evaluates the `expression` on the right side with their use and returns its result.

Examples:
```js
let myFourthFunction = (x) => { 
    statement one;
    statement two;
    // comments about my code
    
    return ___;
};
```
Or
```js
let myFourthFunction = (x) => x * x;
```

- The `()` are optional if only a single argument is passed.



---


## Function Invocation

- The code inside a JavaScript function will execute when "something" invokes it.

- A JavaScript function can be `invoked` without being `called` (think IIFE's) 

---

## Food for Thought

- Wherever JavaScript expects a `statement`, you can also write an `expression`.

- Such a `statement` is called an `expression statement`.

- The reverse does not hold: you CANNOT write a `statement` where JavaScript expects an `expression`.

- For example, an `if-statement` cannot become the `argument` of a `function`.

---

## Miscellaneous 

* A `binding` is a `variable` in JavaScript and requires a name.
  
* An empty `return` statement or the absence of one, causes a function to return a value of `undefined`.

* Function `parameters` vs Function `arguments`?
  * `parameters` are the values a function may <ins>accept</ins>; whereas, `arguments` are the values that are <ins>passed</ins> into a function.

* callback functions

* lambda functions

---

Credits: https://2ality.com/2012/09/expressions-vs-statements.html
