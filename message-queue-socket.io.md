# Message Queue

## Socket.io Chat Example
* Explain to a non-technical recruiter what the Chat Example does.
It recieves a message from the client, then send it to everyone in the network (instant messaging)

* What proof of life are we getting on the backend from the above app?
The backend listens on the connection event for incoming sockets, and logs it to the console.

* Socket.IO gives us the i0.emit() method to send an event to everyone. 
What flag would you use if you want to send a message to everyone except for a certain emitting socket?
io.broadcast()

## Rooms
* What is a room and how might a room be useful?
  * A room is an arbitrary channel that sockets can join and leave. 
  * It can be used to broadcast events to a subset of clients

* How do you join a room?
  * First, name the room 'event' in the server
  * Emit the same 'event' with a payload in the socket
  * Server then takes care of the joining with socket.join

* How do you leave a room?
  * With a differently named event which the server handles with socket.leave

## Namespaces
* What is a Namespace and what does it allow you to do?
  * Like rooms, it is also a communication channel. 
  * Kind of like the parent file to the rooms/handlers/middlewares specified to that channel. 
  * Allows for split logic/cleaner code

* Each namespace potentially has its own what?
  * Client,
  * Server,
  * And the communication pipe / channel

* Discuss a possible use case for separate namespaces
Perhaps you want to create a special namespace that only authorized users have access to.
The logic related to those users is separated from the rest of the application

### References:
* <https://socket.io/docs/v4/rooms>
* <https://socket.io/docs/v4/namespaces/>
* <https://socket.io/docs/v4/emit-cheatsheet/>
* <https://socket.io/get-started/chat>
