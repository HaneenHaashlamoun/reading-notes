# Python Scope & the LEGB Rule

![mir](https://miro.medium.com/max/409/0*hsE2OKgoLM3L6RL6.png)

The LEGB rule is a kind of name lookup procedure, which determines the order in which Python looks up names. For example, if you reference a given name, then Python will look that name up sequentially in the local, enclosing, global, and built-in scope. If the name exists, then you'll get the first occurrence of it.

### Understanding Scope
**Global scope**: The names that you define in this scope are available to all your code.

**Local scope**: The names that you define in this scope are only available or visible to the code within the scope.

## Names and Scopes in Python
When you assign a name, you're either creating that name or modifying it. Python uses the location of the name assignment or definition to associate it with a particular scope. In other words, where you assign or define a name in your code determines the scope or visibility of that name.

![num](https://www.researchgate.net/publication/303337342/figure/fig1/AS:370746640617473@1465404295790/Pythons-scope-hierarchy-and-variable-name-resolution-As-described-in-the-text-multiple.png)

## Python Scope vs Namespace
A namespace is a mapping from names to objects . A scope is a textual region of a Python program where a namespace is directly accessible. ... A namespace determines which identifiers (e.g. variables, functions, classes) are available for use, and a scope defines where — in your written code — a namespace can be accessed.

![](https://www.bestprog.net/wp-content/uploads/2020/07/11_01_02_10_02_01e.jpg)

- Local (or function) scope is the code block or body of any Python function or lambda expression. This Python scope contains the names that you define inside the function. These names will only be visible from the code of the function. It’s created at function call, not at function definition, so you’ll have as many different local scopes as function calls. This is true even if you call the same function multiple times, or recursively. Each call will result in a new local scope being created.

- Enclosing (or nonlocal) scope is a special scope that only exists for nested functions. If the local scope is an inner or nested function, then the enclosing scope is the scope of the outer or enclosing function. This scope contains the names that you define in the enclosing function. The names in the enclosing scope are visible from the code of the inner and enclosing functions.

- Global (or module) scope is the top-most scope in a Python program, script, or module. This Python scope contains all of the names that you define at the top level of a program or a module. Names in this Python scope are visible from everywhere in your code.

- Built-in scope is a special Python scope that’s created or loaded whenever you run a script or open an interactive session. This scope contains names such as keywords, functions, exceptions, and other attributes that are built into Python. Names in this Python scope are also available from everywhere in your code. It’s automatically loaded by Python when you run a program or script.

----------------
# Rolling Dice Examples

![5](https://miro.medium.com/max/1400/1*hunkumplAED_kcA-uPb0bw.png)

Random
There is a package in Python that allows the use of random numbers.

## Program Example 1
Generate a random number from 1 to 6.

Easy peasy. We will just generate a random number from 1 to 6 with the package like this:

>`import random`
>
>`print(random.randint(1,6))`

As you can see, when you run this program, you get a random 
integer from 1 to 6

## Program Example 2
Simulate the rolling of 1000 dice. Now, count the number of times you roll 6. Print that number out.

We can create a function that returns a random number from 1 to 6. Then, we can make a for loop that rolls the dice 1000 times and check if it is a 6.

>`import random`
>
>`count = 0`
>
>`def roll():`
>
>`    return random.randint(1,6)`
>
>`for i in range(1, 1001):`
>
>`    if roll() == 6:`
>
>`        count += 1`
>        
>`print(count)`


If we run this, we will get a number around 170.

    
© Haneen Hashlamoun
