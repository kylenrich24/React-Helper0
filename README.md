# 🌀 React-Helper 🌀

<img src="https://sunscrapers.com/blog/wp-content/uploads/2018/11/1__DOHv30w-0eI-Ysz5U47Yg.png" height=500 width=900>
🌀 &nbsp; React is a javascript library <br>
🌀 &nbsp; React's ultimate purpose is to show content(HTML) to users and handle user interaction<br>
🌀 &nbsp; React on its own isn't a MVC framework; it is only a component of it (V). <br>
<br>
 <img src="https://hackernoon.com/hn-images/1*xa9A0wBaUIfPF57VIo23nA.png" height=260 width=350> 
  <br>

<br>
<br>

<h2> React Key Concepts </h2>
<br>
<h3> The Birth of React </h3>
<h4> JQuery </h4>
 Allows for manipulation of DOM through Javascript<br>
 Traditonally, we used to have HTML after HTML for every single page in an application <br>
<h4> SPA </h4>
 We now focus more on Javascript and less on HTML (data > page) <br>
 Instead of making a request and getting a new HTML document, we stay on one HTML/DOM and focus on Javascript updates. We can render new things without even communicating with the server anymore. 
<br>

<h3> Key Concepts </h3>

<br> 
🌀 &nbsp; Don't touch the DOM 
<br>
<br> 
<ul>
  <li> React will do it (declarative) </li>
  <br>
 <img src="https://i2.wp.com/programmingwithmosh.com/wp-content/uploads/2018/11/lnrn_0201.png?ssl=1" height=200 width=350> 
  <br>
  <li> Imperative - directly changing individual parts of your application in response to user events. It's difficult to see      relationships between these events and edge cases </li>
  <li>Declarative - consider these two operations:</li>
    <ol>
     <li> change the element and add it to the page </li>
     <li> recalculate the layout and move things around </li>
    </ol>
  <li>Just tell react what you want your app to look like and it will take care of it </li>
    <ol>
      <li>i.e this is the 'state' of the app when the button is clicked </li>
      <li> all the states is in one JS object </li>
     <li> based on the 'state' of the app, I will <em>REACT</em> to it </li>
    </ol>
</ul
 <br>
 <img src="https://www.systango.com/blog/wp-content/uploads/2017/05/img_2-1024x613.png" height=200 width=350> 
  <br>
<br>
🌀 &nbsp; Build websites like lego blocks
 <br> 
 <br>
 <br>
 <img src="https://www.techdiagonal.com/wp-content/uploads/2019/08/React-components-blog-image.jpg" height=350 width=350> 
  <br>
 <ul>
  <li>Reusable components - components are just functions that receive 'state' and return <em>JSX</em></li>
 </ul>
 
```javascript
// state example
state = {
 user: Kyle
 isLoggedIn: true
}
```
 
```javascript
// component example
const App = (props) => {
 return JSX
}
```
<br>
🌀 &nbsp; One way data flow
<br> 
<br>
<ul>
 <li>React has 2 parts: state & component</li>
 <li> It creates a virtual DOM using these 2 </li>
 <li> Every time we want to update the DOM, the state of our app has to change</li>
 <li> Data only moves down from the state of our application </li>
</ul>

<br>
🌀 &nbsp; We are only in charge of the UI
<br> 
<br>
<ul>
 <li>Our React app is a blueprint. We can implement it to the web, mobile, etc. React only has to know the views of the mobile and it can render our app there as well.</li>
</ul>
<br>
 <img src="https://res.infoq.com/articles/react-native-introduction/en/resources/21.jpg" height=200 width=350> 
<br>

<br>

## Let's Dive In!
<ol>
 <li>Install Node Js https://nodejs.org/en/</li>
 <li>Open cmd and generate a new react app &nbsp;&nbsp; <em>npx create-react-app myApp</em></li>
 <li>Run <em>npm start</em> to start the app</li>
</ol>

<br>
<p align='center'>
<img src='https://cdn.rawgit.com/facebook/create-react-app/27b42ac/screencast.svg' width='600' alt='npm start'>
</p>

<br>
<img src="https://i.ytimg.com/vi/A4swyDR45SY/maxresdefault.jpg" height=200 width=350> 
<br>

<br>
<ul>
 <li>Babel - coverts latest versions of ES (React uses this) to ES5 (browsers support this)</li>
 <li>Webpack - our React app is essentially just modules of mostly Javascript with some HTML and CSS. Webpack bundles all of this.</li>
</ul>
 
<br>
<h3>Exploring a Create-React-App-Project</h3>
<br>
<img src="https://scotch-res.cloudinary.com/image/upload/dpr_3,w_300,q_auto:good,f_auto/v1557940680/m0jd7trvsgz2lco6o9um.png" height=300 width=350> 
<br>
<ul>
 <li>📙 &nbsp; src - all our source code</li>
 <li>📙 &nbsp; public - all our static files (i.e index.html {our SPA} and images)</li>
 <li>📙 &nbsp; node_modules - all our project dependencies</li>
 <li>📙 &nbsp; package.json - all our project dependencies and configues our project</li>
 <li>📙 &nbsp; package.lock.json - records the exact version of the packages we install</li>
</ul>

<br>
<br>
<h2> Let's Start Coding!</h2>
<br>
<h4>Javascript Module Systems</h4>
This is made possible by webpack. Codes inside a module isn't going to be automatically shared or made available to other modules and vice versa. If we want to get access to other modules, we have to use an import statement-an ES2015 feature.

<br>

index.html

```jsx
// import react and reactdom
import React from 'react'; // components
import ReactDOM from 'react-dom'; // view in the DOM

// create a react component
const App = () => {
 return <div>Hi There!</div>;
}

// take the react component and show it on the screen 
ReactDOM.render(<App/>, document.querySelector('#root')); // inject our component to public/index.html
```
