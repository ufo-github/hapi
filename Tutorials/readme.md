# hapi

![](https://pbs.twimg.com/media/Czg4mcEVQAAAtd6.jpg)

https://hapijs.com/  

## Getting started

> Start by creating a **package.json**:

```sh
$ npm init
``` 

> Install hapi and save it to your package.json dependencies: 

```sh
$ npm install hapi --save
$ npm i -S hapi
``` 

> Create a **server.js** file with the following contents:  

```js
'use strict';
const Hapi = require('hapi');

// Create a server with a host and port
const server = new Hapi.Server();
server.connection({ 
    host: 'localhost', 
    port: 8000 
});

// Add the route
server.route({
    method: 'GET',
    path:'/hello', 
    handler: function (request, reply) {

        return reply('hello world');
    }
});

// Start the server
server.start((err) => {

    if (err) {
        throw err;
    }
    console.log('Server running at:', server.info.uri);
});
``` 

> Launch the application by running **$ npm start** and open **localhost:8000/hello** in your browser.  

## Read more about getting started with hapi  

https://hapijs.com/tutorials  

https://hapijs.com/api  


