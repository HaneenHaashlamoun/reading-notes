# Thinking in React

![react](https://www.codeproject.com/KB/scripting/997133/image2.png)

### How would you break a mock into a component heirarchy?

Break The UI Into A Component Hierarchy:

The first thing you’ll want to do is to draw boxes around every component (and subcomponent) in the mock and give them all names. If you’re working with a designer, they may have already done this, so go talk to them! Their Photoshop layer names may end up being the names of your React components!

But how do you know what should be its own component? Use the same techniques for deciding if you should create a new function or object. One such technique is the single responsibility principle, that is, a component should ideally only do one thing. If it ends up growing, it should be decomposed into smaller subcomponents.

Since you’re often displaying a JSON data model to a user, you’ll find that if your model was built correctly, your UI (and therefore your component structure) will map nicely. That’s because UI and data models tend to adhere to the same information architecture. Separate your UI into components, where each component matches one piece of your data model.

### What is the single responsibility principle and how does it apply to components?
The single-responsibility principle (SRP) is a computer-programming principle that states that every module, class or function in a computer program should have responsibility over a single part of that program's functionality, and it should encapsulate that part. ... Hence, each module should be responsible for each role.
![fg](https://www.logiqlabs.com/wp-content/uploads/2021/04/SRP.png)

### What does it mean to build a ‘static’ version of your application?

What is a Static App? Static applications and websites render in the user's browser without the need for server side processing, this means that all the rendering of HTML, CSS, and JavaScript is done on the client side, rather then relying on server side technologies.

### Once you have a static application, what do you need to add?

Step 1: Add Your New Site
Step 2: Link to Your GitHub (or supported version-control tool of choice)
Step 3: Authorize Netlify
Step 4: Select Your Repo
Step 5: Configure Your Settings
Step 6: Build Your Site
Step 7: All Done
[reference](https://www.netlify.com/blog/2016/10/27/a-step-by-step-guide-deploying-a-static-site-or-single-page-app/)

### What are the three questions you can ask to determine if something is state?
- Is it passed in from a parent via props? If so, it probably isn’t state.
- Does it remain unchanged over time? If so, it probably isn’t state.
- Can you compute it based on any other state or props in your component? If so, it isn’t state.


### How can you identify where state needs to live?

For each piece of state in your application:

- Identify every component that renders something based on that state.
- Find a common owner component (a single component above all the components that need the state in the hierarchy).
- Either the common owner or another component higher up in the hierarchy should own the state.
- If you can’t find a component where it makes sense to own the state, create a new component solely for holding the state and add it somewhere in the hierarchy above the common owner component.



© Haneen Hashlamoun
