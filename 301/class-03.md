# Readig-03 Passing Functions as Props
#### How to Use the Spread Operator (…) in JavaScript
![img](https://miro.medium.com/max/2000/1*24ayqOY008AvW_VmkqsYdA.png)
The spread operator is a useful and quick syntax for adding items to arrays, combining arrays or objects, and spreading an array out into a function’s arguments.

*What is the spread operator?*
InJavaScript, spread syntax refers to the use of an ellipsis of three dots (…) to expand an iterable object into the list of arguments.

*What is ... used for?*
- Spread operator to the rescue! It looks similar to rest parameters

*What else can … do?*
The … spread operator is useful for many different routine tasks in JavaScript, including the following:
- Copying an array
- Concatenating or combining arrays
- Using Math functions
- Using an array as arguments
- Adding an item to a list
- Adding to state in React
- Combining objects
- Converting NodeList to an array
![img](https://miro.medium.com/max/1000/1*oB0L8ezFrNnU9aR55BrEng.png)


## Lists and Keys
![img](https://i.ytimg.com/vi/0sasRxl35_8/maxresdefault.jpg)
*How you transform lists in JavaScript ?*
we use the map() function to take an array of numbers and double their values.

*Rendering Multiple Components*
You can build collections of elements and include them in JSX using curly braces {}.

Below, we loop through the numbers array using the JavaScript map() function. We return a `<li>` element for each item. Finally, we assign the resulting array of elements to listItems

*Keys Must Only Be Unique Among Siblings*
Keys used within arrays should be unique among their siblings. However, they don’t need to be globally unique.

*Embedding map() in JSX*
JSX allows embedding any expression in curly braces so we could inline the map() 

#### Function Increment()
 Increment(): It takes a variable and increments (changes) its value, and also returns this value. The increment can be a positive or negative number.

#### Math functions
The Math object's set of functions are a perfect example of the spread operator as the only argument to a function.

One of the best ways to understand the use of spread operator in JavaScript is to look at the the built-in functions Math.min() and Math.max()

*Using an array as arguments*
Since the spread operator “spreads” an array into different arguments, any functions that accepts multiple any number of arguments can benefit from use of the spread operator.

## What does .map() return?
map() function returns a map object(which is an iterator) of the results after applying the given function to each item of a given iterable (list, tuple etc.) ... fun : It is a function to which map passes each element of given iterable. iter : It is a iterable which is to be mapped.

## If I want to loop through an array and display each value in JSX, how do I do that in React?

It is very popular to use loops like for-loop (in most cases the fastest one), for-in, or for-of to iterate through elements.

That method is useful when we use separate functions to render part of components, and it’s the best method for performance.

The second method that I’ve included in the example is the method with array.forEach().

This method, compared to the for-loops and map method, is the slowest one and doesn’t return the values like a map, so you need to have a special case to use it.

## Each list item needs a unique __key__.

## What is the purpose of a key?
A “key” is a special string attribute you need to include when creating lists of elements in React. Keys are used to React to identify which items in the list are changed, updated, or deleted. In other words, we can say that keys are used to give an identity to the elements in the lists.

--------------------------

# The Spread Operator

![spread](https://i2.wp.com/www.logic24by7.com/wp-content/uploads/2018/11/spreadOperator.png?fit=560%2C315&ssl=1)

### What is the spread operator?
Spread operator allows an iterable to expand in places where 0+ arguments are expected. It is mostly used in the variable array where there is more than 1 values are expected. It allows us the privilege to obtain a list of parameters from an array.

### List 4 things that the spread operator can do.

- Concat()
> `let arr = [1,2,3];`

> `let arr2 = [4,5];`

> `arr = arr.concat(arr2);`

> `console.log(arr); // [ 1, 2, 3, 4, 5 ]`

- Copy(like splice method)
- Expand
- Math

### example of using the spread operator to add a new item to an array.
>`let arr = ['a','b','c'];`

>`arr.push('d');`

>`console.log(arr);//['a','b','c','d']`

### Give an example of using the spread operator to combine two arrays.

>`let arr = ['a','b'];`

>`let arr2 = [arr,'c','d'];`
  
>`console.log(arr2); // [ [ 'a', 'b' ], 'c', 'd' ]`


### example of using the spread operator to combine two objects into one.

>`const user1 = {`

>`name: 'Jen',`

>`age: 22,`

>`};`
  
>`const user2 = {`
    
>`name: "Andrew",`

>`location: "Philadelphia" `

>`};`
  
>`const mergedUsers = {...user1, ...user2};`

>`console.log(mergedUsers)`

OUTPUT
![](https://media.geeksforgeeks.org/wp-content/uploads/20200427163229/Screenshot-from-2020-04-27-16-02-361.png)

[reference](https://www.geeksforgeeks.org/javascript-spread-operator/)

© Haneen Hashlamoun

