Setup for 
React Training Macy's Learning Spike 

Core Audience: Experienced JavaScript developers interested in bringing structure to their rapidly
growing web applications.

Prerequisites: Advanced knowledge of JavaScript that includes Object Oriented concepts,
Ajax, promises, prototypal inheritance, ES6 and module design patterns.

If you don't know ES6, aka ES2015, this is a great free intro course:
CodeSchool ES2015: The Shape of JavaScript to Come
http://campus.codeschool.com/courses/es2015-the-shape-of-javascript-to-come

---
Setup

Install Node.js LTS from https://nodejs.org/

Add node to your path, then
In a terminal, cmd prompt, or powershell:

node -v
Should be >= 8.0

npm -v 
Should be greater than 5.0.

---
For this course you'll need either a Text Editor or an IDE.

Recommended Text Editors:
Visual Studio Code: install from https://code.visualstudio.com/
or
Sublime Text
https://www.sublimetext.com/

---
Recommended IDEs
Jetbrains IDEs, either WebStorm or IntelliJ.
http://www.jetbrains.com/

---
Install eslint
npm install -g eslint

We'll do more setup in class as needed.

---
The Evolution of the Web
http://www.evolutionoftheweb.com/

A Brief History of the Web
https://blog.keepsite.com/a-brief-history-of-the-web-809509ba23df

The (R)Evolution of Web Development by Mark Erikson
http://blog.isquaredsoftware.com/presentations/2016-10-revolution-of-web-dev/#/?_k=8f5q6o

---
Modern Web Development with React and Redux by Mark Erikson
http://blog.isquaredsoftware.com/presentations/2017-02-react-redux-intro/#/23

---
Resources:
Think In React
https://reactjs.org/docs/thinking-in-react.html

---
Course Materials

React Foundation by Azat Mardan
https://github.com/azat-co/react-foundation

Download zip or clone.
---
Course Outline
https://github.com/azat-co/react-foundation/blob/master/README.md

Intro
https://github.com/azat-co/react-foundation/blob/master/react-intro.md
---
Module 1
https://github.com/azat-co/react-foundation/blob/master/react-01.md

Changing the State example
http://plnkr.co/edit/S2gjlc?p=preview

---
Module 2
https://github.com/azat-co/react-foundation/blob/master/react-02.md
---
Module 3
https://github.com/azat-co/react-foundation/blob/master/react-03.md
---
Module 4
https://github.com/azat-co/react-foundation/blob/master/react-04.md
---
React Foundation Summary
https://github.com/azat-co/react-foundation/blob/master/react-outro.md
---
Flux
http://facebook.github.io/flux/docs/in-depth-overview.html#content

---
Redux
https://redux.js.org/

State Management with Redux
http://blog.isquaredsoftware.com/presentations/2017-02-react-redux-intro/#/33
---
Redux Example Incrementer
https://csb-62zvqom7kk-janthncuwn.now.sh/

### Lab: Port Counter State to Redux


Redux Course Notes
https://github.com/tayiorbeii/egghead.io_redux_course_notes

Free Course Videos from Dan Abramov
Learn Redux from its creator:
Part 1: Getting Started with Redux (30 free videos)
https://egghead.io/series/getting-started-with-redux

Part 2: Building React Applications with Idiomatic Redux (27 free videos)
https://egghead.io/courses/building-react-applications-with-idiomatic-redux


Wes Bos Redux Video Course
https://courses.wesbos.com/account/access/5a34aee80e25892227e21408

https://medium.com/netscape/my-recommended-free-resources-to-learn-react-68f4d20a8dc1

Code Sandbox
https://codesandbox.io/s/62zvqom7kk

Zeit for deployment
https://csb-62zvqom7kk-janthncuwn.now.sh

Github Tutorial
http://kbroman.org/github_tutorial/pages/init.html

JS Bin Online Editor
http://jsbin.com/mipesawapi/edit?js,output

Optional Final Project requires many dependencies.

Install MongoDB.   You'll have to download and install MongoDB 
https://docs.mongodb.com/getting-started/shell/tutorial/install-mongodb-on-windows/

Make sure that you created these directories for MongoDB
'''
mkdir c:\data\db
mkdir c:\data\log
'''
You'll have to add to the System Environment Variable PATH
C:\Program Files\MongoDB\Server\3.6\bin\
Launch new Powershell or Cmd prompt.
```
mongod
```
Launch another Powershell or Cmd
```
cd react-foundation\code\autocomplete
```
npm install

This project has many dependencies that need to be updated.
Even after fixing there will likely still be issues.
```
npm install react -D
npm install babel-core -D
npm install babel-loader -D
npm install webpack -D

Warning: Accessing PropTypes via the main React package is deprecated. Use the prop-types package from npm instead.
 npm install prop-types -D
 Then have to change code.
 react-quickly\ch20\autocomplete> npm start

> autocomplete@1.0.0 start C:\Users\david\git\react-quickly\ch20\autocomplete
> npm run build && ./node_modules/.bin/node-dev index.js


> autocomplete@1.0.0 build C:\Users\david\git\react-quickly\ch20\autocomplete
> webpack

Warning: Accessing PropTypes via the main React package is deprecated. Use the prop-types package from npm instead.
Hash: 0f0497b28a0247312aee
Version: webpack 2.4.1
Time: 1037ms
     Asset     Size  Chunks             Chunk Names
    app.js  5.45 kB       0  [emitted]  main
app.js.map  2.62 kB       0  [emitted]  main
   [0] ./src/app.jsx 2.78 kB {0} [built] [failed] [1 error]

ERROR in ./src/app.jsx
Module build failed: ReferenceError: [BABEL] C:\Users\david\git\react-quickly\ch20\autocomplete\src\app.jsx: Unknown option: C:\Users\david\git\react-quickly\ch20\autocomplete\node_modules\react\react.js.Children. Check out http://babeljs.io/docs/usage/options/ for more info
    at Logger.error (C:\Users\david\git\react-quickly\ch20\autocomplete\node_modules\babel-core\lib\transformation\file\logger.js:41:11)
    at OptionManager.mergeOptions (C:\Users\david\git\react-quickly\ch20\autocomplete\node_modules\babel-core\lib\transformation\file\options\option-manager.js:290:20)
    at C:\Users\david\git\react-quickly\ch20\autocomplete\node_modules\babel-core\lib\transformation\file\options\option-manager.js:371:14
    at C:\Users\david\git\react-quickly\ch20\autocomplete\node_modules\babel-core\lib\transformation\file\options\option-manager.js:392:24
    at Array.map (<anonymous>)
    at OptionManager.resolvePresets (C:\Users\david\git\react-quickly\ch20\autocomplete\node_modules\babel-core\lib\transformation\file\options\option-manager.js:387:20)
    at OptionManager.mergePresets (C:\Users\david\git\react-quickly\ch20\autocomplete\node_modules\babel-core\lib\transformation\file\options\option-manager.js:370:10)
    at OptionManager.mergeOptions (C:\Users\david\git\react-quickly\ch20\autocomplete\node_modules\babel-core\lib\transformation\file\options\option-manager.js:330:14)
    at OptionManager.addConfig (C:\Users\david\git\react-quickly\ch20\autocomplete\node_modules\babel-core\lib\transformation\file\options\option-manager.js:232:10)
    at OptionManager.findConfigs (C:\Users\david\git\react-quickly\ch20\autocomplete\node_modules\babel-core\lib\transformation\file\options\option-manager.js:442:30)
    at OptionManager.init (C:\Users\david\git\react-quickly\ch20\autocomplete\node_modules\babel-core\lib\transformation\file\options\option-manager.js:484:12)
    at File.initOptions (C:\Users\david\git\react-quickly\ch20\autocomplete\node_modules\babel-core\lib\transformation\file\index.js:223:65)
    at new File (C:\Users\david\git\react-quickly\ch20\autocomplete\node_modules\babel-core\lib\transformation\file\index.js:140:24)
    at Pipeline.transform (C:\Users\david\git\react-quickly\ch20\autocomplete\node_modules\babel-core\lib\transformation\pipeline.js:46:16)
    at transpile (C:\Users\david\git\react-quickly\ch20\autocomplete\node_modules\babel-loader\lib\index.js:46:20)
    at Object.module.exports (C:\Users\david\git\react-quickly\ch20\autocomplete\node_modules\babel-loader\lib\index.js:163:20)
npm ERR! code ELIFECYCLE
npm ERR! errno 2
npm ERR! autocomplete@1.0.0 build: `webpack`
npm ERR! Exit status 2
npm ERR!
npm ERR! Failed at the autocomplete@1.0.0 build script.
npm ERR! This is probably not a problem with npm. There is likely additional logging output above.
```