# Access Control (ACL)

## 5 steps to RBAC
* What is Role Based Access Control (RBAC)?
  * RBAC is a security model to manage and contol system access based on a user's role in an organization. 
  * This prevents the system from be access by / changes from being made by users without specific permissions.

* Describe a Role/Permission heirarchy that you might implement using RBAC.
Admin -> Managers -> Supervisors -> Employees -> some guy off the street (no permission)

* What approach might you take to implement RBAC?
  * Identify roles
  * Define permissions associated with each role
  * Assign roles and permissions to users
  * Regularly monitor and review the RBAC implementation to ensure its effectiveness 
  * Adjust as needed

* If Authentication is “you are who you say you are,” what is Authorization?
Authorization is "you are allowed to be here"

* Name three primary rules defined for RBAC.
Role Assignment / Permission Assignment / Constraints

* Describe RBAC to a non-technical friend.
  * RBAC is a means of controlling who has access to which specific data in a computer system
  * Users are grouped into roles based on their job, and permissions are ssigned based on these roles
  * This ensures users can only access necessary data, and nothing more

* What are access rights associated with? The User? or The Role? Explain.
  * Access rights are associated with job roles rather than individual users. 
  * Users are assigned to roles, and the permissions associated with that role are applied to the user. 
  * The role assigned to any specific user can be changed as the user's job changes

* Access Rights, or Authorization, is activated after a user successfully does what?
After a user successfuly authenticates their identity

* Explain how RBAC might benefit a business.
I worked at a grocery store before, and the store had a RBAC system implemented. 
When I started as a cashier, the permissions I had on the company computer allowed me to login to my personal account, where I could send emails, ask for time off, check my schedule, etc.
When I was promoted to manager, I was able to see my personal account, as well as the schedule for everyone on my team, my team's time off requests, etc etc.
Certain parts of the store's system did not need to be accessed by eveyone on the team. Cashier Laurel did not need to know who put in a request for time off, and should not have the ability to approve or deny that request.
Manager Laurel needed access to other parts of the system in order to properly take care of the team.

### References:
* <https://www.csoonline.com/article/3060780/5-steps-to-simple-role-based-access-control.html>
* <https://en.wikipedia.org/wiki/Role-based_access_control>
* <https://www.youtube.com/watch?v=C4NP8Eon3cA&ab_channel=Udacity>
