# Node basics

## Common JS modules VS ES6

https://stackoverflow.com/questions/35728117/difference-between-import-http-requirehttp-and-import-as-http-from-htt 

import http = require('http') //Common JS
This is Common JS modules. Before version 12.2, this was the only way to use modules in node JS.

import * as http from 'http'; //ES 6
This is ES6 module. In ECMAScript 6 standards, modules are natively supported by Javascript. Node JS implemented this feature in version 12.2.

Out of these two, I always prefer ES6 module because it is part of javascript implementation. ES6 module is also supported by browser. But Common JS is not supported by browser since it is synchronous. AMD module was used in browser before ES 6 because it is asynchronous unlike CommonJS

## Example of Node.js Application

https://nodejs.org/en/learn/getting-started/introduction-to-nodejs 

const http = require('node:http');
const hostname = '127.0.0.1';
const port = 3000;
const server = http.createServer((req, res) => {
  res.statusCode = 200;
  res.setHeader('Content-Type', 'text/plain');
  res.end('Hello World\n');
});
server.listen(port, hostname, () => {
  console.log(`Server running at http://${hostname}:${port}/`);
});