### Optional Homework: Final Project in React Foundation 
* Requires many dependencies. Won't have time in this short course.
* See <a target="_ref" href=" ">React Quickly Setup</a>

* Install MongoDB.   You'll have to download and install MongoDB 
* <a target="_ref" href="https://docs.mongodb.com/getting-started/shell/tutorial/install-mongodb-on-windows/">MongoDB Windows</a>
* <a target="_ref" href="https://docs.mongodb.com/getting-started/shell/tutorial/">MongoDB Tutorial</a>

---
### MongoDB Continued 
* Make sure that you created these directories for MongoDB

```
mkdir c:\data\db
mkdir c:\data\log
```
* You'll have to add to the System Environment Variable PATH
```
C:\Program Files\MongoDB\Server\3.6\bin\
```
* Launch new Terminal, Powershell or Cmd prompt.
```
mongod
```
---
### Optional Homework project Autocomplete

* Launch another Terminal, Powershell or Cmd
```
cd react-foundation\code\autocomplete
```
* Change babel to babel-loader in webpack.config.js
```
npm install
```
* This project has many dependencies that need to be updated.
* Even after fixing there will likely still be issues.
```
npm install react -D
npm install babel-core -D
npm install webpack -D
```
---
### Optional homework autocomplete issues
* Warning: Accessing PropTypes via the main React package is deprecated. Use the prop-types package from npm instead.
```
 npm install prop-types -D
 ```
 Then have to change code.
``` 
 cd react-quickly\ch20\autocomplete> 
 npm start
```
> autocomplete@1.0.0 start C:\Users\david\git\react-quickly\ch20\autocomplete
> npm run build && ./node_modules/.bin/node-dev index.js
> autocomplete@1.0.0 build C:\Users\david\git\react-quickly\ch20\autocomplete
> webpack
* Warning: Accessing PropTypes via the main React package is deprecated. Use the prop-types package from npm instead.
