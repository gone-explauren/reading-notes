#Authentication

## Securing Passwords
* Explain to a non-technical friend how you would safely hash and store a password.
*Hashing* will turn a password into something that is not a password, so when a hacker hacks the database, the passwords are still safe

* What is Bcrypt?
Bcrypt is an *adaptive hash function* based on the Blowfish symmetric block cipher cryptographic algorithm.

* Why might you use something like Bcrypt?
To make your application more secure

### References
* <https://www.npmjs.com/package/bcrypt>
* <https://thehackernews.com/2014/04/securing-passwords-with-bcrypt-hashing.html>

## Basic Auth
* What is Basic Authentication?
A method for an HTTP user agent (web browser) to provide a username and password when making a request

* What properties are necessary in the header of a Basic Auth request?
  * **Authorization: Basic <credentials>**
  * Credentials is the encoding of *ID* and *password* joined by a single colon :

* How are username:password in Basic Auth encoded?
  * The string is encoded into an octet sequence.
  * It is encoded using a variant of Base64
  * The authorization method and a space character is then prepended to the encoded string

### References:
* <https://en.wikipedia.org/wiki/Basic_access_authentication>

## OWASP Auth Cheatsheet
* Define the authentication process to a non-technical recruiter.
  * The user tries to login, username/id and passowrd are sent to the database.
  * If the credentials match what is expected by the DB, the user is able to access the page.
  * If the credentials don't match, the user is sent an error message

* How should your error messaging respond (both HTTP and HTML)? Why?
Error messages should be generic and non-specific ("Password is incorrect") and give no hints to hackers trying to get into the system

* **Consider OWASP fundamentals any time you interact with authentication.**
* **Applications developed with security in mind from inception have fewer vulnerabilities throughout their lifecycle.**

### References:
* <https://cheatsheetseries.owasp.org/cheatsheets/Authentication_Cheat_Sheet.html>
