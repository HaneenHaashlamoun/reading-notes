# Error Handling & Debugging in JavaScript

![debug](https://cdn.splessons.com/wp-content/uploads/2016/08/jsp-debugging-splessons.jpg)

--------------------------------

What is error handling and debugging?

Errors, bugs, and therefore debugging are a part of life for a programmer. ... Dealing with errors actually involves two very different processes: error handling and debugging. Error handling is a combination of coding and methodology that allows your program to anticipate user and other errors.

- ORDER OF EXECUTION
- EXECUT.ION CONTEXTS
- EXECUTION CONTEXT & HOISTING

![obj](https://miro.medium.com/max/2514/1*s8MYrR4abDGWXrOKDUEFGA.png)

### ERROR OBJECTS

Error objects are thrown when runtime errors occur. The Error object can also be used as a base object for user-defined exceptions.

![errror](https://images.slideplayer.com/31/9700382/slides/slide_25.jpg)


-----------
**HOW TO DEAL WITH ERRORS**
Now that you know what an error is and how the browser treats them, there are two things you can do with the errors.

1. DEBUG THE SCRIPT TO FIX ERRORS
2. HANDLE ERRORS GRACEFULLY

**A DEBUGGING WORKFLOW**
Debugging is about deduction: eliminating potential causes of an error.
Here is a workflow for techniques you will meet over the next 20 pages.
Try to narrow down where the problem might be, then look for clues.

*BROWSER DEV TOOLS & JAVASCRIPT CONSOLE The*
The JavaScript console will tell you when there is a problem with a script,
where to look for the problem, and what kind of issue it seems to be.

--------------

- If you understand execution contexts (which have two
stages) and stacks, you are more likely to find the error
in your code.
- Debugging is the process of finding errors. It involves a
process of deduction.
- The console helps narrow down the area in which the
error is located, so you can try to find the exact error.
- JavaScript has 7 different types of errors. Each creates
its own error object, which can tell you its line number
and gives a description of the error.
- If you know that you may get an error, you can handle
it gracefully using the try, catch, finally statements.
- Use them to give your users helpful feedback.


*******************************

all rights reserved to Copyright: © *HTML & CSS Design and Build Websites* by **Jon Duckett**

