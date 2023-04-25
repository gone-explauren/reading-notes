# AWS S3 and Lambda

## S3
* What is Amazon S3?
Amazon Simple Storage Service is an *object storage service* offering scalability, data availability, security, and performance.

* Name some use cases for Amazon S3.
  * Storing and distributing static assets: S3 can be used to store images, videos, and files that need to be distributed to users.
  * Hosting static websites: S3 can be used to host static websites that do not require server-side processing or database access.
  * Backup and archiving: S3 can be used for backup and archiving of data.

* Name some benefits of using Amazon S3.
  * S3 benefits include:
    * Scalability: S3 can store and retrieve virtually unlimited amounts of data, making it a highly scalable storage solution.
    * Durability: S3 ensures that data is always available when needed.
    * Security: S3 provides access control, encryption, and security policies to protect data.
    * Cost-effective: S3 pricing is based on usage and storage duration.
    * Integration with other AWS services: S3 integrates seamlessly with other AWS services, such as EC2, Lambda, and CloudFront, making it easy to build complex cloud-based applications.


## Lambda
* What is AWS Lambda?
Lambda can be used to create functions to act as middleware for your code in the cloud.

* Name some use cases for AWS Lambdas.
  * Scalable APIs: one execution of a Lambda function can serve a single HTTP request.
  * Data processing: Lambda functions are optimized for event-based data processing.

* Describe “serverless” to a non-technical friend.
A “serverless” service runs an application without managing the underlying infrastructure. The developer can work on developing the software without concern about the server compatibility.

## CDN

* What is a CDN?
A “Content Delivery Network” that consists of geographically distrubuted group of servers that work together to provide fast delivery of internet content.

* How does a CDN work with relation to the website visitor?
When a user requests a webpage that is part of a CDN, the request is redirected to the cached content in the CDN that’s the closest to the user. CDNs communicate with the originating server to deliver any content that has not been previously cached.

* What are the benefits of employing a CDN?
  * Efficiency, 
  * increased reliability, 
  * security

### References:
* <https://aws.amazon.com/s3/>
* <https://www.serverless.com/aws-lambda>
* <https://cyberhoot.com/cybrary/content-delivery-network-cdn/>
