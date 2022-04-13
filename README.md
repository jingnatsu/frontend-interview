# frontend-interview
**1. How many HTTP Methods for RESTful Services?**
- REST APIs enable you to develop all kinds of web applications having all possible CRUD (create, retrieve, update, delete) operations. The primary or most-commonly-used HTTP verbs (or methods, as they are properly called) are POST, GET, PUT, PATCH, and DELETE. These correspond to create, read, update, and delete (or CRUD) operation.

| HTTP Verb        | CRUD           | Entire Collection (e.g. /customers)  | Specific Item (e.g. /customers/{id})
| ---------------- |:--------------:| :------------------------------------| :------------------------------------|
| POST      | Create | 201 (Created), 'Location' header with link to /customers/{id} containing new ID. | 404 (Not Found), 409 (Conflict) if resource already exists..
| GET       | Read | 200 (OK), list of customers. Use pagination, sorting and filtering to navigate big lists. | 200 (OK), single customer. 404 (Not Found), if ID not found or invalid.
| PUT  | Update/Replace	 | 405 (Method Not Allowed), unless you want to update/replace every resource in the entire collection. | 200 (OK) or 204 (No Content). 404 (Not Found), if ID not found or invalid.
| PATCH  | Update/Modify |405 (Method Not Allowed), unless you want to modify the collection itself. | 	200 (OK) or 204 (No Content). 404 (Not Found), if ID not found or invalid.
| DELETE  | Delete | 405 (Method Not Allowed), unless you want to delete the whole collection—not often desirable. |200 (OK). 404 (Not Found), if ID not found or invalid.

Refs: https://restfulapi.net/http-methods
#
**2. How many HTTP request methods?**
-  HTTP defines a set of request methods to indicate the desired action to be performed for a given resource. Although they can also be nouns, these request methods are sometimes referred to as HTTP verbs. Each of them implements a different semantic, but some common features are shared by a group of them: e.g. a request method can be safe, idempotent, or cacheable.

- GET
- HEAD
- POST
- PUT
- DELETE
- CONNECT
- OPTIONS
- TRACE
- PATCH

Ref: 
- https://developer.mozilla.org/en-US/docs/Web/HTTP/Methods
- https://www.w3schools.com/tags/ref_httpmethods.asp
- https://www.geeksforgeeks.org/diffrence-between-put-and-post-http-requests/
- https://www.geeksforgeeks.org/difference-between-put-and-patch-request/

**3. How many way to center a div or text?**
- https://blog.hubspot.com/website/center-div-css#:~:text=There%20are%20three%20ways%20to%20center%20a%20div%20within%20a,horizontally%2C%20vertically%2C%20or%20both.
- https://www.youtube.com/watch?v=87YMCtsBoCM&t=499s&ab_channel=KevinPowell
