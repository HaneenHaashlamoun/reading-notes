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

