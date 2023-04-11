# Bearer Authorization

## Intro to JWT
* What is a JSON Web Token (JWT)?
JWT is a means of securely transmitting information as a json object

* When should we use JSON Web Tokens?
Use JWT for credential authorization, secure information exchange

* Claims are expected in which structural component of a JWT?
In the payload

## Are JWTs Secure?
* If I get a JWT and I can decode the payload, how can we call that secure?
  * a JWT with a payload is meant to be decoded by the proper authority (ie the reciever with the secret)
  * the payload is sent as base-64, not encrypted
  * the JWT tells the receiver that the payload has not changed since it was signed
  * if the payload and token don’t match the payload is not accepted as valid

* If sending a JWT, what must sender and receiver both know? Hint, it’s appended in the signature.
The sender and receiver both have to know the secret (*the secret is appended in the signature*)

* Explain how concatenated content and secret can be sent and received securely to a non-technical recruiter.
  * The sender and receiver both know the hash and the secret
  * You can add the secret to the data you want to send, and apply the hash to it
  * This makes it so no one can read it, other than the person that knows the hash that was used and the secret in order to decode it

## JWTs Explained
* Why use JWT?
  * JWT is open source that anyone can use, 
  * it's well understood, 
  * allows for digitally signed transmissions that you know aren't tampered with,
  * and it's very compact and fast.

* What are the three components (the structure) of a JWT signature?
Header, Payload, Signature

### References
* <https://jwt.io/introduction/>
* <https://stackoverflow.com/questions/27301557/if-you-can-decode-jwt-how-are-they-secure>
* <https://www.youtube.com/watch?v=926mknSW9Lo&ab_channel=Bitfumes>
* <https://www.npmjs.com/package/jsonwebtoken>
* 
