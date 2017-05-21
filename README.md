# setUpForNode


Set up environment & configrations:

Node will be used as: (1) Web server

(2) Node web server will render HTML from React component which we write for front end

(3) Node API server:talk to database

For Windows:

1 Install node and npm: download from https://nodejs.org/en/ and run installer. During the installer running, choose the npm install manager. npm config information can be found at https://docs.npmjs.com/misc/config

2 Test node version: node -v

Test npm version: npm -v

3 In console type : npm init

Create package.json file to store the general information and dependencies for project

4 Start documenting and insttalling dependencies

(1) main dependencies: the packages our code will use as product

1.1 create node web server by using Express.js :

    npm install --save express
1.2 create driver for connecting from node to Mongo

    npm i -S mongodb
1.3 front end using react and react-dom:

    npm i -S react react-dom
(2)dev dependencies : only use in local develop environment

2.1 webpack:the most popular tool that translate modular code into browser understand language

    nmp install --save-dev webpack
2.2 babel: webpack loader that transform JSX extension code into React understand language and JS file that not support by browsers

    npm i -D babel-cli babel-loader babel-preset-es2015 babel-preset-stage-2 babel-preset-react
2.3 nodemon: change can be reload directly without restart the server in the running process

   npm i -D nodemon
2.4 ESLint:allow developers to discover problems with their JavaScript code without executing it

   npm i -D eslint eslint-plugin-react babel-eslint
   
   
 3 Add webpack.config.js, .eslintrc.js and .babelrc into root path
 
 4 Change the path incluing into global path variable
 
  type vi ~/.bash_profile , add below export into file and save
  
  export PATH=$PATH:./node_modules/.bin
  
 5 babel-node server.js
 
 program server.js should run on console


For exist project:
How to use
----------

Run "npm install" inside this project folder to install all dependencies.

Make sure you use the latest version of the CLI (upgrade guide below)

Run "ng serve" to see the app in action.

Feel free to compare it with your project code to spot any errors you might have.


How to upgrade the CLI
-----------------------

Run the below commands - only use "sudo" on Mac/ Linux.

sudo npm uninstall -g angular-cli @angular/cli
npm cache clean
sudo npm install -g @angular/cli
