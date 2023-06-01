# React
### A JS library that allows us to write more JS.

## Why React ?
Traditionally for a website every page has different html file.
Most of the libraries were directly manipulating the dom this way of programming was called imperative programming and it takes a long time to do this as the way it works is like hey this happened now do this then this  n etc etc.


**But React used the following approaches** 

### ***Don’t TOUCH the DOM*** <br>
  React used the declarative approach , all you need to do is just give the blueprint how the page should look like or what will be the state then react here we don’t need to tell what to do it does everything according to the state.


### ***Build websites like LEGO blocks (Components)*** <br>
  The app will have small components which put together which will make large components and then form the full App 
  These components are just plain JS functions which recieves props (arguments) and return html inside the js (JSX).
  They can be used multiple times or you can use prebuilt coponents and modify them according to you needs.


### ***Unidirectional Data Flow*** <br>
  The React app uses virtual DOM and follows a unidirectional data flow, where data only flows from top to bottom.
  This approach simplifies the app's architecture and makes it easier to debug and maintain. React uses virtual DOM to minimize the number of changes made to the actual DOM, which can be a slow and resource-intensive process. Instead, React only updates the virtual DOM and calculates the minimum set of changes needed to update the actual DOM.
  
  This approach also makes it easier to reason about the app's state and to implement complex features like time-travel debugging and server-side rendering. By enforcing a unidirectional data flow, React ensures that the state of the app is predictable and easy to reason about, which makes it easier to implement features like undo and redo.
  Overall, the unidirectional data flow is a key concept in React and is essential to building scalable and maintainable apps.


### ***It is just the UI*** <br>
  React is a versatile platform that can be used to develop applications for a variety of purposes. For example, it can be used in conjunction with React Native to create Android apps, or with React 360 to develop virtual reality applications. 
  
  Additionally, React can be used to create desktop applications using Electron or React Desktop, or even command line interfaces using React Blessed.
  This wide range of possibilities is due to the fact that React has a flexible and adaptable blueprint, which can be customized to meet the needs of different types of applications. Whether you are developing a mobile app, a desktop application, or a command line interface,


# How to be a Great React Developer
- Decide on Components
- Decide the state and where it lives
- What changes when state changes

# NPM vs NPX
NPM downlods the packages locally then it uses them which can take a lot of space so here comes NPX it donwloads the packages and uses them then deletes them so that your environment remains nice.
npm create-react-app will require you to download create-react-app then use it.
