# React Intermediate

## Size of the components

### Not Too Big

![Untitled](images/Untitled.png)

- Too many reponsibilities
- Needs to many props
- Hard to reuse
- Complex code, hard to understand

### Not to small

![Untitled](images/Untitled%201.png)

- We end up with 100s of mini-components
- Confusing Codebase
- Too abstracted (Creating something new to hide the implementation details of that thing)

**Generally we need to find the right balance between too specific and too broad.**

![Untitled](images/Untitled%202.png)

## The 4 criteria for splitting a UI into components:

1. Logical separation of content/layout
2. Reusability 
3. Reponsebilities / Complexity
4. Personal coding style

![Untitled](images/Untitled%203.png)

![Untitled](images/Untitled%204.png)

![Untitled](images/Untitled%205.png)

## Props drilling

Passing props into several child to get the required data.

![Untitled](images/Untitled%206.png)

To get the number of movies in `NumResults` we need to pass the props in `App > ListBox > MovieList` (for the state) and then to the `NavBar`.

## Component Composition

When using a component in another component we can’t reuse the main component.

![Untitled](images/Untitled%207.png)

- ***Component Composition: Combining different components using the children prop (or explicitly defined props)***

### In component composition, we can:

1. Create highly reusable and flexible components
2. Fix prop drilling (great for layouts)

**Possible because the components don’t need to know their children in advance**  

![Untitled](images/Untitled%208.png)

Fixing the prop drilling 

![Untitled](images/Untitled%209.png)

## PropTypes

PropTypes is a way to ensure that components receive the right type of props. It can be used to indicate required props, default values for props, or specific datatypes for props. This can help catch and debug errors during development.

![Untitled](images/Untitled%2010.png)

In the above image the starRating is the component having different props.

# Components vs. Instances vs. Element

- Blueprint or Template
- Function that returns **React elements (element tree)**, usually written in jsx.
- Description of UI
- 

![Untitled](images/Untitled%2011.png)

![Untitled](images/Untitled%2012.png)

# How components are displayed on the screen

![Untitled](images/Untitled%2013.png)

![Untitled](images/Untitled%2014.png)

## How Rendering works: The Render Phase

![Untitled](images/Untitled%2015.png)

![Untitled](images/Untitled%2016.png)

## What is Reconciliation and why do we need it?

Why not update the entire DOM whenever state changes somewhere in the app?

That would be inefficient and wasteful:

- Writing to the dom is slow
- usually only a small part of the DOM needs to be updated.

React reuses as much of the existing DOM as possible by **Reconciliation.**

### Reconciliation:

Deciding which DOM elements actually need to be inserted deleted or updated in order to reflect the latest state changes.

## The Reconciler : FIBER

![Untitled](images/Untitled%2017.png)

## The commit phase and Browser paint

![Untitled](images/Untitled%2018.png)

![Untitled](images/Untitled%2019.png)

# In a nutshell

![Untitled](images/Untitled%2020.png)

## What the hell is Diffing?

- Two elements of different types will produce different trees.
- 

![Untitled](images/Untitled%2021.png)

- Elements with a stable key prop stay the same across render.
- 

![Untitled](images/Untitled%2022.png)

# The Key Prop

- Special prop that we use to tell the diffing algorithm that an element is unique
- Allows React to distinguish between multiple instances of the same component type
- When a key stays the same across renders, the element will be kept in the DOM (even if the position in the tree changes)
    - Using keys in lists
- When a key changes between renders, the elements will be dsstroyed and a new one will be created (even if the position in the tree is the same as before)
    - Using keys to reset state
    
    ## Keys in Lists [stable key]
    
    ![Untitled](images/Untitled%2023.png)
    
    ## Keys prop to Reset State[changing key]
    
    ![Untitled](images/Untitled%2024.png)
    

# The two types of Logic in React Components

![Untitled](images/Untitled%2025.png)

### Functional Programming

**Side Effect :**  Dependency on or modification of any data outside the function scope. “Interaction with the outside world”. Example: mutating external variables, HTTP requests, writing to DOM. 

```jsx
const areas = {};
function circleArea(r) {
areas.circle = 3.14 * r * r;
}
```

**Pure function :** a function that has no side effects.

- Does not change any variable outside its scope
- Given the same input, a pure function always returns the same output.

```jsx
function circleArea(r){
 const date = Date.now();
 const area = 3.14 * r * r;
 return `${date} ${area}`;
 }
```

### Components must be pure when it comes to render logic:

Given the same props(input), a component instance should always return the same JSX(output)

### Render logic must produce no side effects:

No interaction with the “outside world “ is allowed. So, in render logic:

- Do not perform network requests  (API calls)
- Do not start timer
- Do not directly use the DOM API
- Do not mutate objects or variables outside of the functions scope
- Do not update state(or refs): this will create an infinite loop

### Batched state update in react

![Untitled](images/Untitled%2026.png)
