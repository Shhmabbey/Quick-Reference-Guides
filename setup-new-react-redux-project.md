Model your project folder to look like the directory tree below:
  index.html
  bundle.js (no need to create this file, webpack will create it for you)
  frontend
    * actions
    * components
    * reducers
    * store
    * util
    todo_redux.jsx
  
Create entry file and package.json
```
touch index.js
npm init -y
```

Install webpack and install the npm packages that you will be using to create your React/Redux app:
```
npm install -D webpack webpack-cli 
npm install react react-dom redux react-redux @babel/core babel-loader @babel/preset-react @babel/preset-env
```

Set up your webpack.config.js file so that your bundle.js is saved in the root directory of your project.
```
touch webpack.config.js
```
See sample below: 
```
{
  "name": "w11d2-redux",
  "version": "1.0.0",
  "description": "",
  "main": "index.js",
  "scripts": {
    "test": "echo \"Error: no test specified\" && exit 1",
    "start": "webpack --watch --mode=development"
  },
  "keywords": [],
  "author": "",
  "license": "ISC",
  "dependencies": {
    "@babel/core": "^7.18.6",
    "@babel/preset-env": "^7.18.6",
    "babel-loader": "^8.2.5",
    "redux": "^4.2.0",
    "webpack": "^5.73.0",
    "webpack-cli": "^4.10.0"
  }
}
```

Test your setup
```
npm run start
```
Set up your entry file index.jsx to render ```<h1>TESTING</h1>``` into your root page's #content container.
Open index.html and confirm that it worked.




