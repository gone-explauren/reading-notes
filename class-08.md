# API Design Best Practices

## What does REST stand for?
* REpresentational State Transfer

## REST APIs are designed around a ____.
* Resource (ie data, objects, etc that can be accessed be a client)

## What is an identifier of a resource? Give an example.
* URI (Unique Resource Identifier)
* a unique string of characters used to identify a specific resource

## What are the most common HTTP verbs?
* GET, 
* POST,
* PUT,
* DELETE,
* PATCH, and 
* OPTIONS

## What should the URIs be based on?
* URIs should be based on the resources that they represent
* ex: mywebsite.com/shop

What does it mean to have a ‘chatty’ web API? Is this a good or a bad thing?
* A chatty API makes multiple requests to do a single function.
* This is a bad thing because it can take a long time to process these requests

## Status code 200: **successful GET request**

## Status code 201: **successful POST request**

## Status code 204: **successful DELETE request**

## Status codes 400 (401, 404, etc): **unsuccessful GET request**

### References:

* <https://learn.microsoft.com/en-us/azure/architecture/best-practices/api-design>
