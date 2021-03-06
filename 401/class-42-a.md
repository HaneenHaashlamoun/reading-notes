#  Pythonisms

## [Dunder Methods](https://dbader.org/blog/python-dunder-methods)

## What Are Dunder Methods?
![d](https://miro.medium.com/max/1090/1*adNnLBEuZce4cee6Q8LUSw.png)
In Python, special methods are a set of predefined methods you can use to enrich your classes. They are easy to recognize because they start and end with double underscores, for example `__init__` or `__str__`.

## Enriching a Simple Account Class

Throughout this article I will enrich a simple Python class with various dunder methods to unlock the following language features:

- Initialization of new objects
- Object representation
- Enable iteration
- Operator overloading (comparison)
- Operator overloading (addition)
- Method invocation
- Context manager support (with statement)

## Object Initialization: __init__
Right upon starting my class I already need a special method. To construct account objects from the Account class I need a constructor which in Python is the __init__ dunder:
```
    class Account:
        """A simple account class"""

        def __init__(self, owner, amount=0):
            """
            This is the constructor that lets us create
            objects from this class
            """
            self.owner = owner
            self.amount = amount
            self._transactions = []
```

## Operator Overloading for Comparing Accounts: __eq__, __lt__

We all write dozens of statements daily to compare Python objects:
```
    >>> 2 > 1
    True

    >>> 'a' > 'b'
    False
```
## Operator Overloading for Merging Accounts: __add__

In Python, everything is an object. We are completely fine adding two integers or two strings with the + (plus) operator, it behaves in expected ways:

    >>> 1 + 2
    3

    >>> 'hello' + ' world'
    'hello world'


## Callable Python Objects: __call__

You can make an object callable like a regular function by adding the __call__ dunder method. For our account class we could print a nice report of all the transactions that make up its balance:

    class Account:
        # ... (see above)

        def __call__(self):
            print('Start amount: {}'.format(self.amount))
            print('Transactions: ')
            for transaction in self:
                print(transaction)
            print('\nBalance: {}'.format(self.balance))



## Python 2.x Compatible Iterators
All the code examples I showed here were written in Python 3. There???s a small but important difference between Python 2 and 3 when it comes to implementing class-based iterators:

In Python 3, the method that retrieves the next value from an iterator is called __next__.
In Python 2, the same method is called next (no underscores).
This naming difference can lead to some trouble if you???re trying to write class-based iterators that should work on both versions of Python. Luckily there???s a simple approach you can take to work around this difference.

Here???s an updated version of the InfiniteRepeater class that will work on both Python 2 and Python 3:

    class InfiniteRepeater(object):
        def __init__(self, value):
            self.value = value

        def __iter__(self):
            return self

        def __next__(self):
            return self.value

        # Python 2 compatibility:
        def next(self):
            return self.__next__()

## Python Generators ??? A Quick Summary

- Generator functions are syntactic sugar for writing objects that support the iterator protocol. Generators abstract away much of the boilerplate code needed when writing class-based iterators.
- The yield statement allows you to temporarily suspend execution of a generator function and to pass back values from it.
- Generators start raising StopIteration exceptions after control flow leaves the generator function by any means other than a yield statement.


## Python Generators 101 ??? The Basics

This is what the class looked like in its second (simplified) version:

    class Repeater:
        def __init__(self, value):
            self.value = value

        def __iter__(self):
            return self

        def __next__(self):
            return self.value

![s](https://lh3.googleusercontent.com/proxy/KO-YiXuhng3oj9wV0iSZO6KX2cL9cxoZAmUX45B1FKRFp3qP3rlQ2F_U-tL76dzlgYAPbMl86vbFF2fURqK0EDHxx4p9T0ZDM4RqfoAX-qObiTGd8JB2am0g3puJXTOqsn-VlMet9nbbmLzn8O67R6zJ_w)

## Python Generators That Stop Generating

Thankfully, as programmers we get to work with a nicer interface this time around. Generators stop generating values as soon as control flow returns from the generator function by any means other than a yield statement. This means you no longer have to worry about raising StopIteration at all!

Here???s an example:

    def repeat_three_times(value):
        yield value
        yield value
        yield value

