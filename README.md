### Welcome to React Training
#### Instructor: David Marsland
<br>
<img src="http://www.developintelligence.com/sites/all/themes/diresponsive/images/Develop-Intelligence-logo-f.png">
<br>
<a target="_di" href="http://developintelligence.com">DevelopIntelligence.com</a>
<br>
<a target="_git_react" href="https://davidmarsland.github.io/react-spike/">https://davidmarsland.github.io/react-spike/</a>

---
### React Training
* Core Audience: Experienced JavaScript developers interested in bringing structure to their rapidly growing web applications

* Prerequisites: Advanced JavaScript that includes Object Oriented concepts, Ajax, promises, prototypal inheritance, ES6 and module design patterns

* If you don't know ES6, aka ES2015, here are some good tutorials:
  * <a target="_babel" href="https://babeljs.io/learn-es2015/">https://babeljs.io/learn-es2015/</a>
  * <a target="_udacity" href="https://www.udacity.com/course/es6-javascript-improved--ud356
  ">ES6 - JavaScript Improved | Udacity</a>

---
### Lab Setup

Install Node.js LTS from <a target="_setup" href="https://nodejs.org/">https://nodejs.org/</a>

Add node to your path, then
In a terminal, cmd prompt, or powershell:

```
node -v
```
Should be >= 8.0
```
npm -v
``` 
Should be greater than 5.0.

Install eslint
```
npm install -g eslint
```
We'll do more setup in class as needed.

---
### For this course you'll need either a Text Editor or an IDE.

#### Recommended Text Editors:
* Visual Studio Code: install from <a target="_setup" href="https://code.visualstudio.com/">https://code.visualstudio.com/</a>
* Sublime Text
<a target="_setup" href="https://www.sublimetext.com/">https://www.sublimetext.com/</a>

---
### Recommended IDEs (not needed, Text Editor preferred)
Jetbrains IDEs, either WebStorm or IntelliJ.
<a target="_setup" href="http://www.jetbrains.com/">http://www.jetbrains.com/</a>

---
### Introducing your instructor, David Marsland
<a target="_ref" href="https://www.linkedin.com/in/davidemarsland">https://www.linkedin.com/in/davidemarsland</a>
<br>
<br>
Web Development since the Dawn of the Web <br>
<a target="_ref" href="https://web.archive.org/web/19970616152144fw_/http://reality.sgi.com:80/mars_corp/"><img src="https://web.archive.org/web/19971210071250im_/http://reality.sgi.com:80/images/sgipowered.gif" />
<br>Wayback Machine 1997 reality.sgi.com/mars_corp</a>

---
### Life after SGI
* Sun Java Certified Developer and Instructor 1998-2004
* eBay Chief Instructor 2004-2009
* Sencha Chief Instructor / Training Director 2010-2015
* Marsland Enterprises Chief Instructor 2015-
* DevelopIntelligence Senior Technical Instructor 2017-

---
### Hello React World

<p data-height="565" data-theme-id="0" data-slug-hash="jYWpNR" data-default-tab="js,result" data-user="demarsland" data-embed-version="2" data-pen-title="Hello React World" class="codepen">See the Pen <a href="https://codepen.io/demarsland/pen/jYWpNR/">Hello React World</a> by David Marsland (<a href="https://codepen.io/demarsland">@demarsland</a>) on <a href="https://codepen.io">CodePen</a>.</p>
<script async src="https://production-assets.codepen.io/assets/embed/ei.js"></script>

---
### The Evolution of the Web
<a target="_ref" href="http://www.evolutionoftheweb.com/">http://www.evolutionoftheweb.com/</a>

### A Brief History of the Web
* <a target="_ref" href="https://blog.keepsite.com/a-brief-history-of-the-web-809509ba23df">A Brief History of the Web</a>

* <a target="_ref" href="http://blog.isquaredsoftware.com/presentations/2016-10-revolution-of-web-dev/#/?_k=8f5q6o">The (R)Evolution of Web Development by Mark Erikson</a>

---
### Naming Conventions

* React doesn't enforce naming conventions
* There are many different approaches to class and file naming
* <a target="_ref" href="https://github.com/airbnb/javascript/tree/master/react#naming">Airbnb React/JSX Style Guide</a> shows one approach

---
### React Dev Labs

### Lab solutions are available here:
<a target="_git_labs" href="https://github.com/davidmarsland/react-labs/">https://github.com/davidmarsland/react-labs/</a>

Clone this repo into the directory you want to save the course labs:
```
git clone https://github.com/davidmarsland/react-labs/
```
Then
```
cd react-labs
mkdir labs

cd solutions
cd catalog3cart
npm install
npm run start
```

---
### Tutorial Labs Overview: Intro to React
<a target="_ref" href="https://reactjs.org/tutorial/tutorial.html">Facebook React Tutorial</a>

---

### Lab: Set Up React Dev Env and Create React App helloworld
* Follow the steps in this tutorial to use Create React App for starter files
  <a target="_ref" href="https://www.kirupa.com/react/setting_up_react_environment.htm">https://www.kirupa.com/react/setting_up_react_environment.htm</a>
* Then create helloworld app inside <code>react-spike/labs</code> directory
  ```
  create-react-app helloworld
  ```


---
### Thinking In React
<a target="_ref" href="https://reactjs.org/docs/thinking-in-react.html">https://reactjs.org/docs/thinking-in-react.html</a>

---
### Lab: Simple Table in React
#### Implement a simple table in React
* Generate project in labs directory

  ```
  create-react-app simpletable
  ```
* In src directory, delete App.*
* Start with this data from Thinking In React and declare PRODUCTS in src/index.js

```
const PRODUCTS = [
  {category: 'Sporting Goods', price: '$49.99', stocked: true, name: 'Football'},
  {category: 'Sporting Goods', price: '$9.99', stocked: true, name: 'Baseball'},
  {category: 'Sporting Goods', price: '$29.99', stocked: false, name: 'Basketball'},
  {category: 'Electronics', price: '$99.99', stocked: true, name: 'iPod Touch'},
  {category: 'Electronics', price: '$399.99', stocked: false, name: 'iPhone 5'},
  {category: 'Electronics', price: '$199.99', stocked: true, name: 'Nexus 7'}
];
```

* In src directory, create file SimpleTable.jsx

  ```
  import React from 'react';

  class SimpleTable extends React.Component {
    render() {
      return (
        <table>
          <tbody>
          </tbody>
        </table>
      )
    }
  }

  export default SimpleTable;
  ```

* Inside the tbody tags use an array and map() this.props.products to populate the name and price for each product

  ```
  <tr><td>name</td><td>price</td></tr>
  ```

<br>Similar to this:

  ```
    <ul>
      {this.props.items.map((value, index) => {
        return <li key={index}>{value}</li>
      })}
    </ul>
  ```

* Modify index.js to render SimpleTable instead of App and pass in products={PRODUCTS} as a prop.
* Run app in browser

```
npm start
```

---
### Setting Up Your React Dev Environment Easily 
* Create React App simplifies setup 
* <a target="_ref" href="https://www.kirupa.com/react/setting_up_react_environment.htm">https://www.kirupa.com/react/setting_up_react_environment.htm</a>
* <a target="_ref" href="https://github.com/facebookincubator/create-react-app/blob/master/packages/react-scripts/template/README.md">Create React App Docs</a>

---
### Lab: Thinking In React Filterable Product Table Catalog
* Read the <a target="_ref" href="https://reactjs.org/docs/thinking-in-react.html">Thinking in React Tutorial</a> up to Step 2
* Generate project 

  ```
  create-react-app catalog
  ```

* Modularize the code in 
<a target="_ref" href="https://codepen.io/gaearon/pen/BwWzwm">Step 2: Build A Static Version in React</a>

* In src directory, delete App.*
* Start with this data from Thinking In React and declare PRODUCTS in src/index.js

```
const PRODUCTS = [
  {category: 'Sporting Goods', price: '$49.99', stocked: true, name: 'Football'},
  {category: 'Sporting Goods', price: '$9.99', stocked: true, name: 'Baseball'},
  {category: 'Sporting Goods', price: '$29.99', stocked: false, name: 'Basketball'},
  {category: 'Electronics', price: '$99.99', stocked: true, name: 'iPod Touch'},
  {category: 'Electronics', price: '$399.99', stocked: false, name: 'iPhone 5'},
  {category: 'Electronics', price: '$199.99', stocked: true, name: 'Nexus 7'}
];
```

* In src directory, create jsx files for each class and add import and export like this:

  `ProductCategoryRow.jsx`

  ```
  import React from 'react';

  class ProductCategoryRow extends React.Component {
  ...
  export default ProductCategoryRow;
  ```

* Import appropriate dependencies for each file like this:

  ```
  import React from 'react';
  import ProductCategoryRow from './ProductCategoryRow';
  import ProductRow from './ProductRow';

  class ProductTable extends React.Component ...
  ```
* Modify index.js to import FilterableProductTable then render.  <br>
Note that id is 'root', not 'container'

  ```
  ReactDOM.render(
    <FilterableProductTable products={PRODUCTS} />,
    document.getElementById('root')
  );
  ```
* Run app in browser

  ```
  npm start
  ```
---
### Lab: Add State to Filterable Product Table
* Read all of <a target="_ref" href="https://reactjs.org/docs/thinking-in-react.html#step-3-identify-the-minimal-but-complete-representation-of-ui-state">Step 3:  Identify The Minimal (but complete) Representation Of UI State</a>
* Read <a target="_ref" href="https://reactjs.org/docs/thinking-in-react.html#step-4-identify-where-your-state-should-live">Step 4: Identify Where Your State Should Live</a>
<br>and modify the code as described to add state
* Complete <a target="_ref" href="https://reactjs.org/docs/thinking-in-react.html#step-5-add-inverse-data-flow">Step 5: Add Inverse Data Flow</a>
* Optional Challenge: Create a Cart component and add selected products to the cart

  ```
  handleAddToCart(product) {
      this.setState({
        cart: this.state.cart.concat(product)  
        // returns a new array
      })
    }
  ```
* Optional Challenge: use your own test data for real shopping! 

---
### React Foundation Course Materials

#### React Foundation by Azat Mardan
<a target="_reactf" href="https://github.com/azat-co/react-foundation">
https://github.com/azat-co/react-foundation</a>

### Download zip or clone.
### Github Tutorials

* <a target="_ref" href="https://try.github.io">CodeSchool Free tryGit Interactive Tutorial</a>
* <a target="_ref" href="http://kbroman.org/github_tutorial/pages/init.html">Github Guide</a>


---
### Free Video Courses on Node University
* <a target="_nodeu" href="https://node.university/courses/category/free">https://node.university/courses/category/free</a>
### This course includes material from Azat Mardan's React Foundation Course with Videos
<a target="_react_foundation" href="https://node.university/p/react-foundation">https://node.university/p/react-foundation</a>

---
### React Quickly Book
#### by Azat Mardan
<a target="_react-quickly" href="https://livebook.manning.com/#!/book/react-quickly">React Quickly Livebook</a>

---
### React Foundation Course
* <a target="_react" href="https://github.com/azat-co/react-foundation/blob/master/README.md">Course Outline</a>

* <a target="_react" href="https://github.com/azat-co/react-foundation/blob/master/react-intro.md">Course Intro</a>

---
### React Foundation Course Modules
* <a target="_react" href="https://github.com/azat-co/react-foundation/blob/master/react-01.md">Module 1 Hello React World</a>
* <a target="_plunk" href="http://plnkr.co/edit/S2gjlc?p=preview">Changing the State example</a>
* <a target="_react" href="https://github.com/azat-co/react-foundation/blob/master/react-02.md">Module 2 Components</a>
* <a target="_react" href="https://github.com/azat-co/react-foundation/blob/master/react-03.md">Module 3 User Input</a>
* <a target="_react" href="https://github.com/azat-co/react-foundation/blob/master/react-04.md">Module 4 Advancing Components</a>
* <a target="_react" href="https://github.com/azat-co/react-foundation/blob/master/react-outro.md">React Foundation Summary</a>

---

### CommonJS import/require module.exports vs. ES6 modules import/export

* React Foundation Course uses Node CommonJS module
* Why?  Can use same syntax with server-side Node and Client side

* <a target="_ref" href="voidcanvas.com/import-vs-require/">voidcanvas.com/import-vs-require/</a>
* <a target="_ref" href="https://livebook.manning.com/#!/book/react-quickly/appendix-e/136">React Quickly Appendix E: ES6 Modules</a>
> Azat Mardan wrote: "Personally, I find ES6 modules confusing. Yes, they’re more eloquent, but Node.js modules won’t change anytime soon. It’s better to have only one style for browser and server JavaScript, so I’ll stick with CommonJS/Node.js style for now. In addition, support for ES6 modules in browsers isn’t available as of this writing, so you’ll need something like jspm (<a target="_ref" href="http://jspm.io">http://jspm.io</a>) to use ES6 modules.

> For more information and examples, see <a target="_ref" href="http://exploringjs.com/es6/ch_modules.html">http://exploringjs.com/es6/ch_modules.html</a>. And no matter what, 
> write modular JavaScript!"

---
### Flux
<a target="_ref" href="http://facebook.github.io/flux/docs/in-depth-overview.html#content">Flux from Facebook

---
### Redux
<a target="_ref" href="https://redux.js.org/">redux.js.org</a>

<a target="_ref" href="http://blog.isquaredsoftware.com/presentations/2017-02-react-redux-intro/#/33">
State Management with React and Redux</a>

---
### Redux example and Lab
<a target="_ref" href="https://csb-62zvqom7kk-janthncuwn.now.sh/">
Redux Example Incrementer</a>

---
### Free Course Videos from Dan Abramov
#### Learn Redux from its creator:

* <a target="_ref" href="https://egghead.io/series/getting-started-with-redux">Part 1: Getting Started with Redux (30 free videos)</a>

* <a target="_ref" href="https://egghead.io/courses/building-react-applications-with-idiomatic-redux">Part 2: Building React Applications with Idiomatic Redux (27 free videos)</a>

#### Redux Course Notes
* <a target="_ref" href="https://github.com/tayiorbeii/egghead.io_redux_course_notes">Redux Course Notes https://github.com/tayiorbeii/egghead.io_redux_course_notes</a>

---

### Redux Todo Example App from Redux Course 
* <a target="_redux" href="https://github.com/sadams/todo-redux-react-webpack">https://github.com/sadams/todo-redux-react-webpack</a>
* Clone repo, then:
```
npm install
npm run start
```
* Launches on localhost:8080 by default.

---

### Optional Lab: Catalog with React and Redux
* Port your simple catalog in React to use Redux for state management
* Previously, you modularized this code <a target="_ref" href="https://reactjs.org/docs/thinking-in-react.html">Thinking in React Shopping https://reactjs.org/docs/thinking-in-react.html</a>
* Refactor to use Redux 
* Use Todo Redux example for inspiration <a target="_redux" href="https://github.com/sadams/todo-redux-react-webpack">https://github.com/sadams/todo-redux-react-webpack</a>
* See previous page for setup
* Optional challenges: use your own test data for real shopping! 

---
### More React and Redux Learning Resources

* <a target="_ref" href="https://www.fullstackreact.com/30-days-of-react/">FullStack React 30 Days of React and Redux</a>

* <a target="_ref" href="https://www.fullstackreact.com/articles/react-tutorial-cloning-yelp/">React Tutorial: Cloning Yelp</a>

* <a target="_ref" href="http://cabin.getstream.io/">Learn React & Redux With Cabin</a>

* <a target="_ref" href="https://survivejs.com/react/introduction/">Survive JS - Webpack and React Book</a>

---
### Useful Tools 

* Grip server, preview GitHub Markdown files like README.md locally
* <a target="_ref" href="https://github.com/joeyespo/grip">https://github.com/joeyespo/grip</a>
---
### Redux Video Course by Wes Bos

* <a target="_ref" href="https://courses.wesbos.com/account/access/5a34aee80e25892227e21408">Wes Bos Redux Video Course</a>

* <a target="_ref" href="https://medium.com/netscape/my-recommended-free-resources-to-learn-react-68f4d20a8dc1">Free Resources to Learn React</a>
* <a target="_ref" href="https://livebook.manning.com/#!/book/react-quickly/">React Quickly book by Azat Mardan</a>
* <a target="_ref" href="https://livebook.manning.com/#!/book/react-quickly/chapter-9">React Quickly Free Chapter Menu Project</a>

* <a target="_ref" href="https://egghead.io/series/getting-started-with-redux">Part 1: Getting Started with Redux (30 free videos)</a>

* <a target="_ref" href="https://egghead.io/courses/building-react-applications-with-idiomatic-redux"> Part 2: Building React Applications with Idiomatic Redux (27 free videos)</a>

---
### Tools
* <a target="_ref" href="https://codesandbox.io/s/62zvqom7kk">Code Sandbox</a>

* <a target="_ref" href="https://csb-62zvqom7kk-janthncuwn.now.sh">Zeit for deployment</a>

* <a target="_ref" href="http://jsbin.com/mipesawapi/edit?js,output">JS Bin Online Editor</a>

---
### Github Tutorial
* <a target="_ref" href="http://kbroman.org/github_tutorial/pages/init.html">Github tutorial</a>


---
### Routing in React
* Package react-router 
* <a target="_ref" href="https://reacttraining.com/react-router/">https://reacttraining.com/react-router/</a>
* <a target="_ref" href="https://github.com/ReactTraining/react-router">https://github.com/ReactTraining/react-router</a>
<a target="_ref" href="https://github.com/reactjs/react-router-tutorial">react-router tutorial https://github.com/reactjs/react-router-tutorial</a>
---
### Routing with Backbone and React
* <a target="_ref" href=" ">React Quickly has a Backbone routing example in Ch. 13</a>
* <a target="_ref" href="https://github.com/azat-co/react-quickly/tree/master/ch13">https://github.com/azat-co/react-quickly/tree/master/ch13</a>
### Backbone router to render React components by doing the following:
* Defining a router class with the routes object as a mapping from URL fragments to functions
* Rendering React elements in the methods/functions of the Backbone Router class
* Instantiating and starting the Backbone the Router object
---
### React Native Intro
<a target="_ref" href="https://www.slideshare.net/ModusJesus/intro-to-react-native">Intro to React Native</a>
---
### Resources to learn more
* <a target="_ref" href="http://reactquickly.co/demos">http://reactquickly.co/demos</a>
* <a target="_ref" href=" ">Review React Foundation Course Videos from Azat Mardan</a>
<a target="_react-quickly" href="https://livebook.manning.com/#!/book/react-quickly">React Quickly Book by Azat Mardan: Livebook</a>
* <a target="_ref" href=" ">React Quickly Summaries</a>

---

### Optional Homework
<a target="_ref" href="mongolab">Optional Homework: Final Project in React Foundation</a>

---

### React and Redux Resources

* <a target="_ref" href="https://www.robinwieruch.de/tips-to-learn-react-redux/">Tips to learn React + Redux in 2018</a>

* <a target="_ref" href="https://thinkster.io/tutorials/learn-redux/">Thinkster: Learn The Fundamentals of Redux</a>
<br>Note, to do the labs you will have to change git commands similar to this:

```
git clone -b 00 https://github.com/gothinkster/react-redux-realworld-example-app.git

```

---

#### PluralSight React Skills Assessment
15 minute test of your proficiency in React.  Should be able to take once with 1 redo.

<a target="_ref" href="https://www.pluralsight.com/paths/react">https://www.pluralsight.com/paths/react</a>

---
### Congratulations, you are now all React Developers!

<a target="_di" href="http://developintelligence.com"><img src="http://www.developintelligence.com/sites/all/themes/diresponsive/images/Develop-Intelligence-logo-f.png">
</a>
<br>
<a target="_git_react" href="https://davidmarsland.github.io/react-spike/">https://davidmarsland.github.io/react-spike/</a>
### Thanks, please fill out course eval now, comments appreciated
