# API Integration

## Review of API Server Build

* Explain the different between a query string parameter and a path parameter.
  * A **query string parameter** is a key-value pair appended to the end of a URL using a question mark “?” and separated by ampersands “&”.
  * A **path parameter** is a part of the URL path that identifies a specific resource or endpoint, denoted by a placeholder surrounded by curly braces “{}”. 
    * Path parameters are used to pass dynamic values within the URL structure.

* What would our API URL with a path id parameter be given the following information:
    * Domain: http://our-site.com
    * v3
    * model name: stuff
    * id: things
      * http://our-site.com/v3/stuff/things

* We have created a dynamic API with an “interface”. Describe how that interface works to a non-technical friend.
  * The interface is what the user interacts with. The interface allows the user to interact with the API and make requests to manipulate data seen on the page.

### References:

* <https://codefellows.github.io/code-401-javascript-guide/curriculum/apps-and-libraries/api-server/>

## Review of Auth Server Build

* Describe how you would use middleware to implement basic and bearer auth.
  * Auth middleware would require the user to be authenticated (ie by logging in) before accessing any other part of the site.

* Describe the handshake necessary to implement OAuth.
  * Client sends a POST request with request body through the HTTP request header
  * The decrypted username and password must match what is stored in the database

* Describe how Role Based Access Control works to a non-technical friend.
  * When a user logs in, their RBAC credentials are sent with the request to be authorized
  * The role determines how much rights the user have over the database

### References

* <https://codefellows.github.io/code-401-javascript-guide/curriculum/apps-and-libraries/auth-server/>
