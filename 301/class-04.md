# React and Forms

![react](https://spectrum.imgix.net/communities/80f42aff-3d86-4945-838c-c819563f24d7/ae2e590e-da7b-49a7-8802-e6a6cd30abcf-4ca6c18545eeda73c850f344e04b2d605731640364f3556cc91d205094e40980-I.png?w=256&h=256&dpr=2&auto=compress&expires=1623456000000&ixlib=js-1.3.0&s=e59b8a720a0bc9f2f14aa6212c58e407)


### What is a ‘Controlled Component’?
A controlled component is a component that renders form elements and controls them by keeping the form data in the component's state. In a controlled component, the form element's data is handled by the React component (not DOM) and kept in the component's state.


### Should we wait to store the users responses from the form into state when they submit the form OR should we update the state with their responses as soon as they enter them? Why.
We should storeupdate the state with their responses as soon as they enter them , Also, since setState() automatically merges a partial state into the current state, we only needed to call it with the changed parts.

### How do we target what the user is entering if we have an event handler on an input field?
The oninput event occurs when an element gets user input.
This event occurs when the value of an `<input>` or `<textarea>` element is changed.
Tip: This event is similar to the onchange event. The difference is that the oninput event occurs immediately after the value of an element has changed, while onchange occurs when the element loses focus, after the content has been changed. The other difference is that the onchange event also works on `<select>` elements.


## The Conditional (Ternary) Operator Explained
![react](https://media.geeksforgeeks.org/wp-content/uploads/20190920110229/Conditional-or-Ternary-Operator-__-in-C_C.jpg)

The conditional (ternary) operator is the only JavaScript operator that takes three operands: a condition followed by a question mark ( ? ), then an expression to execute if the condition is truthy followed by a colon ( : ), and finally the expression to execute if the condition is falsy.

### Why would we use a ternary operator?
Use the ternary operator to simplify your if-else statements that are used to assign values to variables. The ternary operator is commonly used when assigning post data or validating forms.

### Rewrite the following statement using a ternary statement:
     
>`if(x===y){`
    
>`console.log(true);`

>`} else {`

>`console.log(false);}`

this
>`(x===y) ? true : false.`



## Things I want to know more about
ternary statement react
 


© Haneen Hashlamoun

