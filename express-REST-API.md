# Express Rest API

## Review: ES6 Classes
* Classes are a template for creating ____.
An object

* Can a class declaration be hoisted?
No

* How would you describe a constructor and contextual “this” to a non-technical friend?
A Constructor is used to create an Object. *this* is used to access the Object was created when used in the right context.

### References:
* <https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Classes>

## Using Express Routing
* Within Express, what does routing refer to?
Routing refers to the way an application’s endpoints (URIs) respond to client requests.

* What is the difference between a route path and a route method?
  * Route method: derived from the HTTP methods, and is attached to an instance of the express class
  * Route paths: define the endpoints at which requests can be made
    * Route paths can be strings or regular expressions.

* When is it appropriate to add next as a parameter to a route handler and what must you do if next has been passed to your middleware as a parameter?
If you are using middleware, you must invoke *next* to pass the code through the route. Middleware must also have *req* and *res* passed as a parameter along with next

### References:
* <https://expressjs.com/en/guide/routing.html>

## Express Routing
* What is an Express Router?
It is an espress app with only the routing code

* By what means do we initialize express.Router() in an express server?
**var router = express.Router();**

* What do we use route middleware for?
Route middleware is used to process requests and validate parameters passed in

### References:
* <https://www.digitalocean.com/community/tutorials/learn-to-use-the-new-router-in-expressjs-4>
