# Socket.IO

## Web Sockets
* What is a Web Socket?
  * A computer communications protocol that runs over a TCP connection 
  * Allows for continuous, real-time data transfer between client and server 

* Describe the Web Socket request/response handshake and what happens once the connection is established.
  * First, an HTTP request is sent from the client to the server, which responds back with an HTTP response. 
  * After this, the connection is established and the protocol switches to a binary protocol.

* Web Sockets provide a standardized way for the server to send content to a client without first receiving a ____ from that client.
**Request**

## Socket.IO
* What does the event handler io.on() do?
It handles connections, disconnections, and events that happen within those triggers.

* Describe some possible proof of life or proof that the code works as expected
Console logs that trigger from connection/disconnection events.

* What does socket.emit() do?
  * socket.emit() is a function in the Socket.IO library 
  * It sends a message from the server to a connected client or from the client to the server. 
  * It takes an event name and optional data as arguments, allowing for custom events and data exchange between the two parties.

## Socket.io vs Web Sockets
* What is the difference between WebSocket and Socket.IO? (think Git and GitHub, or OAuth and Auth0).
  * WebSocket is the communications protocol that allows communcation between client and server over a TCP connection.
  * Socket.IO is a library that helps to facilitate *real-time communication* between client and server. It uses WebSocket protocol to provide that interface.

* When would you use Socket.IO?
When you need an easy way to have peer-to-peer connection with scaling and browser compatibility

* When would you use WebSockets?
If you want to implement real-time communication when a library like Socket.io is not available.

### References:
* <https://en.wikipedia.org/wiki/WebSocket>
* <https://www.tutorialspoint.com/socket.io/>
* <https://www.educba.com/websocket-vs-socket-io/>
* <https://www.youtube.com/watch?v=vv4y_uOneC0&ab_channel=TechTerms>
* <https://www.youtube.com/watch?v=xMtP5ZB3wSk&ab_channel=SunnyClassroom>
* <https://socket.io/docs/v4/>
* <https://socket.io/docs/v4/server-api>
* <https://socket.io/docs/v4/client-api>
* <https://socket.io/get-started/chat>
* <https://amritb.github.io/socketio-client-tool/>
