#  Introduction to React and Components
![react](https://i1.wp.com/www.codelivly.com/wp-content/uploads/2021/08/fe0nxci7uiln3j04d0i3.jpg?fit=1000%2C420&ssl=1)

--------------------

### What is a Component?
A component is a modular, portable, replaceable, and reusable set of well-defined functionality that encapsulates its implementation and exporting it as a higher-level interface.

A component is a software object, intended to interact with other components, encapsulating certain functionality or a set of functionalities. It has an obviously defined interface and conforms to a recommended behavior common to all components within an architecture.

A software component can be defined as a unit of composition with a contractually specified interface and explicit context dependencies only. That is, a software component can be deployed independently and is subject to composition by third parties.

### Characteristics of Components

- Reusability

- Replaceable

- Not context specific

- Extensible

- Encapsulated

- Independent

### Advantages

- Ease of deployment

- Reduced cost

- Ease of development

- Reusable

- Modification of technical complexity

- Reliability

- System maintenance and evolution

- Independent

# What is “Props” and how to use it in React?

## What is Props?

**React is a component-based library** which divides the UI into little reusable pieces. In some cases, those components need to communicate (send data to each other) and the way to pass data between components is by using **props**.

**“Props”** is a special keyword in React, which stands for **properties** and is being used for **passing data from one component to another**.

> But the important part here is that data with props are being passed in a **uni-directional flow**. (one way from parent to child)

## Using Props in React

1. Firstly, define an attribute and its value(data)
2. Then pass it to child component(s) by using Props
3. Finally, render the Props Data

**You can also learn how to use Props by watching my tutorial video below:**
Props can only be passed to components in one-way (parent to child)

## How are props used in React?
Props are an important technique for passing the read-only attributes to React components. These are usually required to use correctly in the component. The components may not behave as expected If it is not used correctly. Hence, props are required to use props validation in improving react components.

## What is the flow of props?
There are basically two ways that data gets handled in React: props and state (available through this.state ). A third is context, not discussed here, which is more advanced and not currently guaranteed stable (React Docs: Context).

As if sending data to a great-grandchild the following would have to occur...

- Parent sends props to Child
- Child sends props to Grandchild
- Grandchild sends props to GreatGrandChild
## Things I want to know more about

REACT components and dataflows


© Haneen Hashlamoun