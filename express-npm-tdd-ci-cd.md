# Express, NPM, TDD, CI/CD

## Intro to Node.js and Exppress
* Explain middleware, answer as though I were a non-technical recruiter.
Middleware is a program that acts as a moderator between programs. It takes a request, processes it, and passes it to the *next* piece of middleware.

* Express the most popular __ __ ____.
**Node web framework**

* Express is “unopinionated.” What does that mean?
It has fewer restrictions, which leads to more flexibility in solving various problems outside its regular scope

* What is a module and why is modularity useful to us as developers?
A module is code written in one file which you can use inside another file by using require(). Code is cleaner and easier to read when modules are separated into different files.

### References:
* <https://developer.mozilla.org/en-US/docs/Learn/Server-side/Express_Nodejs/Introduction>
* <https://nodejs.org/en/docs>
* <https://expressjs.com/en/4x/api.html>

## What is NPM?
* What version of npm are you running on your machine?
9.5.1

* What command would you type to install a library/package called ‘jshint’ into your node project?
npm i jshint

### References:
* <https://docs.npmjs.com/about-npm>
* <https://docs.npmjs.com/>

## What is TDD?
* Explain why tests are important. Please explain as though I were your non technical elder.
Tests are important because it allows a dev to ensure their code is working in the ways it should be

* What are three expected benefits of testing
  * Squash bugs earlier in development, reduce defective code
  * Less time spent debuggin in final phases of development 
  * Generally improved design qualities in the code

* Name at lest 2 individual pitfalls and at least 2 team pitfalls commonly encountered while writing tests.
  * Individual:
    * not enough and/or too many tests at once
    * test written for trival code (excessive uneccessary tests)
  * Team:
    * poor maintenance of the test suite
    * lack of cocsistent use of the written tests

### References:
* <https://www.agilealliance.org/glossary/tdd/#q=~(infinite~false~filters~(postType~(~'page~'post~'aa_book~'aa_event_session~'aa_experience_report~'aa_glossary~'aa_research_paper~'aa_video)~tags~(~'tdd))~searchTerm~'~sort~false~sortDirection~'asc~page~1)>

## CI/CD
* What are three benefits of Continuous Integration?
  * CI automates much/all of the manual human intervention required to get new code from commit to production.
  * Build, test, and deployment happens automatically after code is written.
  * Improvements in productivity and efficiency, while decreasing development complexity.

* What is the difference between Continuos Delivery and Continuous Deployment?
  * Continuous Delivery queues up the written code and packages with everything it needs to deploy, including the testing infrastructure.  
  * Continuous Deployment is the last step of automating the deployment of the continuous delivery system and getting it out to production quickly.

* Explain how GitHub fits into this process assuming the listener comes from a non-technical background
GitHub is a space where many developers can work simultaneously on a project. Each time a dev commits new code to the project repository, the code can be reviewed before being merged into the main project. There are often tests that must be passed before the code can be merged aqnd deployed.

### References:
* <https://github.com/ladjs/supertest>
* <https://www.restapitutorial.com/httpstatuscodes.html>
