Model the project folder to look like the directory tree below:
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
See sample package.json below: 
```
{
  "name": "project",
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

Install webpack and install the npm packages that will be used to create the React/Redux app:
```
npm install -D webpack webpack-cli 
npm install react react-dom redux react-redux @babel/core babel-loader @babel/preset-react @babel/preset-env
```

Configure webpack.config.js so that the bundle.js is saved in the root directory of your project.
```
touch webpack.config.js
```
See sample below: 
```
const path = require('path');

module.exports = {
  context: __dirname,
  entry: './frontend/todo_redux.jsx',
  output: {
    path: path.resolve(__dirname),
    filename: 'bundle.js'
  },
  module: {
    rules: [
      {
        test: /\.jsx?$/,
        exclude: /(node_modules)/,
        use: {
          loader: 'babel-loader',
          query: {
            presets: ['@babel/env', '@babel/react']
          }
        },
      }
    ]
  },
  devtool: 'source-map',
  resolve: {
    extensions: [".js", ".jsx", "*"]
  }
};
```

Create a .gitignore for your node modules and bundled files
```
touch .gitignore
```

Test your setup
```
npm run start
```
Set up your entry file index.jsx to render ```<h1>TESTING</h1>``` into your root page's #content container.
Open index.html and confirm that it worked.




