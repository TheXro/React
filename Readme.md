# React

React uses virtual dom

so when some component is changed it only changes that particular thing

Components based js library

we build independent and reusable components

and then combine them to make a full fleged website

Class-based components and functional components

class-based are history

## Functional based

```jsx
import React from 'react'
const Example = () => {
	return <div<Hello World!</div>
}
```

the syntac in react is known as JSX

you can directly use js code in simple looking html 

e.g.

```jsx
import './App.css';

const App = () => {
  const name = 'React';
  const isNameShowing = false ;
  return (
    
    <div className="App">
      <h1>Hello, {isNameShowing ? name :  'someone'}</h1>
    </div>
  );
}

export default App;
```

## Creating a react App

There are many ways to create a react app

document.creareelement(”h1”)

h1.innerhtml……….

.append to append the 

three type of react reactdom react native react 3d

cdn , webpack parser

`const head = react.createElement{"h1",{},"hello"}`

`const root = reactdom.createRoot{"h2",{}."h3hh3"}`

now to make the h1 in root we use append

`root.render(head)`

## react fragment

<>  </> just like an empty div

why fragment

ist a rule that if want to render two different elements then we use them 

```jsx
import './App.css';

const App = () => {
  const name = 'React';
  const isNameShowing = false ;
  return (
    
    <div className="App">
      <> //if dont use this then it will give error
	      <h1>Hello, {isNameShowing ? name : 'someone'}</h1>
	      <h2>Goodbye, {name}</h2>
			</>
    </div>
  );
}

export default App;
```

requested a url with /home the view will reqest the modal (database)  then it will send the data to mvt 

## components

a piece of code that returns a peice of jsx

to create a component we use following syntax

```jsx
import './App.css';

const Ravi = () => { //make sure to start the name from capital letters thats how you know its react components
  return (
    <div>
      <h1>Name: Ravi</h1>
      <h2>Age: 20</h2>
      <h3>Address: India</h3>
      <h4>Gender: Male</h4>
      <h5>Marital Status: Single</h5>
    </div>
  )
}

//above we created the Ravi component now we can use it as many time as we want

const App = () => {
  return (
    <div className="App">
      <Ravi /> //this is how you use a component
      <Ravi />
      <Ravi />
      <Ravi />
    </div> 
  );
}

export default App;
```

## Props

pass dymanic data through react components

changing the value of 

they passed by attributes

short of property

```jsx
import './App.css';

const Hmmm = (props) => {
  return (
    <div>
      <h1>Name: {props.name}</h1>
      <h2>Age: {props.age}</h2>
    </div>
  )
}

const App = () => {
  return (
    <div className="App">
      <Hmmm name="johnny" age="44"/>
      <Hmmm name="mia" age="30"/>
      <Hmmm name="angela" age="34"/>
    </div> 
  );
}

export default App;
```

## useState and useEffects

to change the state of the element

```jsx
//import the useState
import { useState } from 'react';

// syntax const [name, setterFun] = useState(inital value);
const App = () => {
  const [counter, setCounter] = useState(0);

//useEffect(() => {
    //setCounter(100);
  }, []); //we need second parameter to run this function only once when the page loads and not every time the counter changes it is called dependency array
useEffect(() => {
    alert("Counter changed to " + counter);
  }, [counter]);

  return (
    <div className="App">
      <button onClick={() => setCounter(counter - 4)}>-</button>
      <h1> {counter} </h1>
      <button onClick={() => setCounter(counter + 7)}>+</button>
    </div>
  );
};

export default App;
```

never modify a state manually

## 

```jsx
import "./App.css";
// import { useState,useEffect } from "react";

// // const Hmmm = (props) => {
// //   return (
// //     <div>
// //       <h1>Name: {props.name}</h1>
// //       <h2>Age: {props.age}</h2>
// //     </div>
// //   );
// // };

// // const App = () => {
// //   return (
// //     <div className="App">
// //       {/* <Hmmm
// //         name="johnny"
// //         age="44" />
// //       <Hmmm
// //         name="mia"
// //         age="30" />
// //       <Hmmm
// //         name="angela"
// //         age="34" />
// //     </div> */}
// //   );
// // };

// const App = () => {
//   const [counter, setCounter] = useState(0);

//   // useEffect(() => {
//   //   setCounter(100);
//   // }, []); //we need second parameter to run this function only once when the page loads and not every time the counter changes it is called dependency array
  
//   useEffect(() => {
//     alert("Counter changed to " + counter);
//   }, [counter]); //

//   return (
//     <div className="App">
//       <button onClick={() => setCounter(counter - 4)}>-</button>
//       <h1> {counter} </h1>
//       <button onClick={() => setCounter(counter + 7)}>+</button>
//     </div>
//   );
// };

// export default App;
```

# NODE

import , required

nodomain

nodmone

get post 

req res 

middleware

function

require()
