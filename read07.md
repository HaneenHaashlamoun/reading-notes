# JavaScript (JS) 

## (Expressions and operators)

![JavaScript](https://globalfuture.solutions/wp-content/uploads/2019/06/javascript-frameworks.jpg)

----------------------------------

## Functions 

A JavaScript function is a block of code designed to perform a particular task.

A JavaScript function is executed when "something" invokes it (calls it).

----------------------

## Defining functions

### Function Declarations vs. Function Expressions :

What is Function Statement/Declarations in JavaScript?
The function statement declares a function.
A declared function is “saved for later use”, and will be executed later, when it is invoked (called).
Just as Variable Declarations must start with “var”, Function Declarations must begin with “function”.


##### What is a Function Expression?
A JavaScript function can also be defined using an expression.
A function expression can be stored in a variable:
var x = function (a, b) {return a * b};
After a function expression has been stored in a variable, the variable can be used as a function. Functions stored in variables do not need function names. They are always invoked (called) using the variable name.

- Function declarations load before any code is executed while Function expressions load only when the interpreter reaches that line of code.
- Similar to the var statement, function declarations are hoisted to the top of other code. Function expressions aren’t hoisted, which allows them to retain a copy of the local variables from the scope where they were defined.

--------------------------

#### Benefits of Function Expressions
There are several different ways that function expressions become more useful than function declarations.
- As closures
- As arguments to other functions
- As Immediately Invoked Function Expressions (IIFE)

--------------------------

© Haneen Hashlamoun


------------------------------





