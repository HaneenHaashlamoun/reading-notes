# Classes and Objects

![g](https://techaid24.com/wp-content/uploads/2020/10/How-To-Construct-Classes-and-Objects-In-Python.jpg)

- Objects are an encapsulation of variables and functions into a single entity. Classes are essentially a template to create your objects

- Accessing Object Variables or Object 
>myobjectx.variable myobjectx.ObjectInside

- You can create multiple different objects that are of the same class(have the same variables and functions defined)

## Thinking Recursively in Python

- any error we face , should break them down into smaller chunks trivial enough to solve. that is Thinking Recursively haw everything going , step by step (algorithm )
- recursive algorithm ; we can divide the steps and call the function

- If the current problem represents a simple case, solve it. If not, divide it into subproblems and apply the same strategy to them.
- houses = ["Eric's house", "Kenny's house", "Kyle's house", "Stan's house"] # Each function call represents an elf doing his work def deliver_presents_recursively(houses): # Worker elf doing his work if len(houses) == 1: house = houses[0] print("Delivering presents to", house) # Manager elf doing his work else: mid = len(houses) // 2 first_half = houses[:mid] second_half = houses[mid:] # Divides his work among two elves deliver_presents_recursively(first_half) deliver_presents_recursively(second_half)

- recursive function: Decompose the original problem into simpler instances of the same problem. This is the recursive case:

> n! = n x (n−1) x (n−2) x (n−3) ⋅⋅⋅⋅ x 3 x 2 x 1 n! = n x (n−1)!
- As the large problem is broken down into successively less complex ones, those subproblems must eventually become so simple that they can be solved without further subdivision. 

## Maintaining
- to maintain state during recursion you have to either: Thread the state through each recursive call so that the current state is part of the current call’s execution context Keep the state in global scope like sum , we want revious value to be saved Maintaining

- Recursive Data Structures in Python A data structure is recursive if it can be deﬁned in terms of a smaller version of itself.

#### Return a new list that is the result of # adding element to the head (i.e. front) of input_list def attach_head(element, input_list): return [element] + input_list attach_head(1, # Will return [1, 46, -31, "hello"] attach_head(46, # Will return [46, -31, "hello"] attach_head(-31, # Will return [-31, "hello"] attach_head("hello", [])))) # Will return ["hello"]

- Starting with an empty list, you can generate any list by recursively applying the attach_head function, and thus the list data structure can be defined recursively as:

- Recursion can also be seen as self-referential function composition. We apply a function to an argument, then pass that result on as an argument to a second application of the same function, and so on. Repeatedly composing attach_head with itself is the same as attach_head calling itself repeatedly

## Python Testing with pytest: Fixtures and Coverage

![6](https://miro.medium.com/max/2000/1*2SYweCRRh6bJPPx8ofgyTQ.png)

- Fixtures

    - When you're writing tests, you're rarely going to write just one or two. Rather, you're going to write an entire "test suite", with each test aiming to check a different path through your code. In many cases, this means you'll have a few tests with similar characteristics, something that pytest handles with "parametrized tests".

    -But in other cases, things are a bit more complex. You'll want to have some objects available to all of your tests. Those objects might contain data you want to share across tests, or they might involve the network or filesystem. These are often known as "fixtures" in the testing world, and they take a variety of different forms.

    - In pytest, you define fixtures using a combination of the pytest.fixture decorator, along with a function definition

- Coverage

    - This is all great, but if you've ever done any testing, you know there's always the question of how thoroughly you have tested your code. After all, let's say you've written five functions, and that you've written tests for all of them. Can you be sure you've actually tested all of the possible paths through those functions?

    
© Haneen Hashlamoun
