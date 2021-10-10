# Test Driven Development (TDD) with Python

![test](https://miro.medium.com/max/2842/1*vEvTMaMTLMVxdpkwOyanQw.png)

## Unit tests and TDD?
Unit tests are some pieces of code to exercise the input, the output and the behaviour of your code. You can write them anytime you want.
But Test-Driven Development is a strategy to think (and write!) tests first.

Other thing to care about is the structure. A convention widely used is the AAA: Arrange, Act and Assert.
- Arrange: you need to organize the data needed to execute that piece of code (input);
- Act: here you will execute the code being tested (exercise the behaviour);
- Assert: after executing the code, you will check if the result (output) is the same as you were expecting.

The Cycle
I hope at this time you didn’t give up of this text because this is an example of an important thing about TDD: the cycle.
The cycle is made by three steps:
- 🆘 Write a unit test and make it fail (it needs to fail because the feature isn’t there, right? If this test passes, call the Ghostbusters, really)
- ✅ Write the feature and make the test pass! (you can dance after that)
- 🔵 Refactor the code — the first version doesn’t need to be the beautiful one

### TDD is not about the money/tests
More than any checking, we need to think about our software design first.


------------------------------
## What does the if __name__ == “__main__”: do?

![name](https://i.ytimg.com/vi/sugvnHA7ElY/maxresdefault.jpg)

If the python interpreter is running that module (the source file) as the main program, it sets the special `__name__` variable to have a value `“__main__”`. If this file is being imported from another module, `__name__` will be set to the module’s name. Module’s name is available as value to `__name__`global variable. 

----------------------------
## Recursive Functions in Python

![](https://cdn.programiz.com/cdn/farfuture/6i17bRQT6hWIqw9JE5rMMyW527g7It_68T7kSzpIplo/mtime:1591262415/sites/tutorial2program/files/python-recursion-function.png)


A recursive function is a function defined in terms of itself via self-referential expressions. This means that the function will continue to call itself and repeat its behavior until some condition is met to return a result.

![rec](https://cdn.programiz.com/sites/tutorial2program/files/python-factorial-function.png)


© Haneen Hashlamoun
