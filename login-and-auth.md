# <Login /> and <Auth />

## Role-Based Access Control (RBAC)

* What is Role Based Access Control (RBAC)?
  * Role Based Acess Control (RBAC) is a security model that provides a structured and efficient approach to managing access rights within an application or system. 
  * **It is a method of controlling access to resources based on the roles assigned to individual users or groups.**

* Share some an example of RBAC including all possible CRUD operations and correlating roles.
  * Admin
    * create, read, update, delete
  * Editor 
    * read, create, update
  * User 
    * read, create
  * Guest 
    * read

* What are the Benefits of RBAC?
  * Employees are only allowed to access the information necessary to effectively perform their job duties. 
  * Access can be based on several factors, such as authority, responsibility, and job competency. 
  * In addition, access to computer resources can be limited to specific tasks such as the ability to view, create, or modify a file.
  * Using RBAC will help in securing your company’s sensitive data and important applications.

### References:

* <https://www.digitalguardian.com/blog/what-role-based-access-control-rbac-examples-benefits-and-more>

## React-Cookie VS React-Cookies

* Describe some **react-cookie** features.
  * Hooks-based API:
    * react-cookie provides the hooks like 'useCookies' and 'useCookie' that allow you to easily access and manipulate cookies within functional components
  * Typed Cookies:
    * supports TypeScript and provides type definitions for cookies, which can help with type safety and editor autocompletion
  * Server-side rendering support:
    * react-cookie supports server-side rendering environments, allowing you to work with cookies on both the client and server sides seamlessly
  * Lightweight:
    * react-cookie has a small footprint and minimal dependencies, making it suitable for projects with strict size contraints

* Describe some **react-cookies** features.
  * Functional and class components support:
    * supports both functional and class coponents allowing toy to work with cookies regardless of the component type
  * Cross-browser compatibility:
    * handles cross-browser inconsistencies and provides a consistent API for working with cokkies across different browsers
  * Dependency-free:
    * no external dependencies, making it lightweight and easy to integrate into our React projects

### References

* <https://www.npmjs.com/package/react-cookie>
* <https://www.npmjs.com/package/react-cookies>
