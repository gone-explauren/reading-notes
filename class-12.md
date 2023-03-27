# Status Codes Based on REST methods

## Status Codes
* 100’s = Information 
  * receipt of the request
* 200’s = Success!
* 300’s = Redirection 
  * ie, to another server
* 400’s = Client Error 
  * unauthorized or invalid request, incorrect URL
* 500’s = Internal Server Error 
  * client request OK, but server could not complete for one reason or another
  
## What is a status code 202? 
* Accepted for asynchronous processing

## What is a status code 308? 
* Permanent Redirection - client must use a different URL to access that route

## What code would you use if an update didn’t return data to a client? 
* 204 - No Content

## What code would you use if a resource used to exist but no longer does? 
* 410 - Gone, resource deleted or moved

## 404: ‘Forbidden’ status code

### References:
* <https://www.moesif.com/blog/technical/api-design/Which-HTTP-Status-Code-To-Use-For-Every-CRUD-App/>


# Build a REST API

## Why do we need to pull our MongoDB database string out of our server and put it into our .env?
* To protect our key and keep it secret

## What is middleware?
* A request handler with access to the app's request-response cycle.

## What does app.use(express.json()) do?
* Parses incoming JSON data to put in a request body

## What does the /:id mean in a route?
* It is a parameter for the route

## What is the difference between PUT and PATCH?
* PUT: replaces an entire object with an updated version of it
* PATCH: keeps the same object but applies changes to that object, a patch

## How do you make a default value in a schema?
* Use the keyword 'Default' when declaring the schema

## What does a 500 error status code mean?
* There is an error with the server

## What is the difference between a status 200 and a status 201?
* 200: success
* 201: ‘successfully created object,' specifically

### References: 
* <https://www.youtube.com/channel/UCFbNIlppjAuEX4znoulh0Cw>
