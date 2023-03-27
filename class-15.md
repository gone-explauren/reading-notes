# OAuth

## What is OAuth?
* Open Standard Authorization
* Allows servers the ability to authenticate the access of a user to the assets based on authentication of the user. 

## Give an example of what using OAuth would look like.
* The user will login and OAuth will validate their authorization and determine if thy are authorized to use this app or this feature of the app.

## How does OAuth work? What are the steps that it takes to authenticate the user?
* User's ID is sent for authorization at login
* A request token is generated
* This token is used by the user's client software and is presented to the authorizing provider
* The request token is "traded" for an approved access token and is presented to the original app the user is trying to access
* The user is able to access the content of the app

## What is OpenID?
* A means for users to use SSO to access multiple sites rather than using multiple credentials across those sites.

### References:
* <https://www.csoonline.com/article/3216404/what-is-oauth-how-the-open-authorization-framework-works.html>


# Authorization and Authentication flows

## What is the difference between authorization and authentication?
* Authorization: Is the User allowed to access this?
* Authentication: Is the User who they say they are?

## What is Authorization Code Flow?
* The exchange of the authorization code for a token which permits the user to access the data

## What is Authorization Code Flow with Proof Key for Code Exchange (PKCE)?
* It is an enhanced authorization code flow that introduces a 'secret' in addition to the token that must be validated by an authorization server.

## What is Implicit Flow with Form Post?
* OAuth for public clients, or apps which can’t store a client's secrets

## What is Client Credentials Flow?
* A system that authenticates and authorizes instead of user

## What is Device Authorization Flow?
* A system used by input constrained devices that access the internet

## What is Resource Owner Password Flow?
* Username/Password that self-authenticates
* **This is** ***not recommended*** **for strong security**

### References:
* <https://auth0.com/docs/get-started/authentication-and-authorization-flow>
* <https://auth0.com/docs/libraries/auth0-react>
