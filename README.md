# JSproject

This project aims at identifying the needs & dependencies for a basic app project written in JavaScript.
It starts from a basic package.json file. The command :

  npm install

executed in the project folder will automatically install all the packages needed for our project in a folder called 
"node_modules". These modules can be completed with the following useful packages :

1. Webpack : -> Requires webpack.config.js - Produces app.bundle.js file in dist/ folder.

 Webpack is a bundler which allows to compile our code and package it into one single file. In order to compile our code,
 we create a file webpack.config.js at the root of our project. It serves at configuration for Webpack in order to know how
 to compile our code. Here, the file states that Webpack is going to use ./src/index.js as our entry point and to bundle it
 into the final file located in ./dist/app.bundle.js. Finally, the package.json file has to point to webpack as we try to
 run a script with npm.
 
 npm install webpack webpack-cli --save-dev

2. Babel : -> produces polyfill.bundle.js file - Allows to provide modifications to our code during execution

 Babel is a transpiler and allows all navigators to support the version of our JavaScript code. It is defined by rules to
 be added in the webpack.config.js file
  
 npm install --save-dev babel-loader @babel/core @babel/preset-env babel-polyfill
  
3. Webpack-dev-server: Launches our app at http://localhost:8080/
  
 Webpack-dev-server is a server aimed to test our code and reload it automatically as soon as changes occur. It only requires
 the "start" command to point to webpack-dev-server in the package.json file in order to call it via "npm start" in our
 terminal.
  
  npm install webpack-dev-server --save-dev
  
 Now that our app has the right dependencies and packages, we may run
 
  npm run build
  
 in the terminal in order to build our project. This will create bundled file called "app.bundle.js". If we want to make
 changes to our app, we may just launch 
 
  npm start
  
 in our terminal and edit our app locally.
 
