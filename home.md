

# Enonic XP websocket extension library #

## Purpose ##

Make Websockets integration with EnonicXP easy and more dynamic. 

This library extends the Enonic XP websocket library with additional features to
make socket integration easier to handle on the server side. The library includes both client side and server side libraries

The library's primary purpose is to allow communication with JSON objects, but it also comes with additional features like multiple handlers, 
expansion, easy group management and a built in event driven add-on. 


## Usage ##

Create a handler for both server side and client side to manage web socket communication

```javascript
//Server side
var ws = require('/lib/wsUtil');

ws.openWebsockets(exports);

// Your server side logic goes here

``` 

```javascript
// Client side
var cws = new ExpWS();


// Your client side logic goes here

```


## How it works ##

The route to the websocket library goes to some URL and binds the ExpWs object to the ``window`` object
```html
<script src="someURL/clientlib.js"></script> <!-- Not a web socket request --> 
```
The handler source is then loaded to the client
```html
<script src="someURL/clientHandler.js"></script> 
```
The handler source create a new ExpWS instance that opens a web socket connection

```javascript
var cws = new ExpWS(); // <-- Request to same route as clientlib.js but with web socket enabled
```

The library will now serve the request as a web socket request and start web socket communication


## Contents ##

[Server API](server.html)

[Client API](client.html)

[Tutorials](tutorial.html)

[Creating extensions](extensions.html)

