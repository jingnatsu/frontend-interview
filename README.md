# frontend-interview
1. How many HTTP Methods for RESTful Services?
- REST APIs enable you to develop all kinds of web applications having all possible CRUD (create, retrieve, update, delete) operations. The primary or most-commonly-used HTTP verbs (or methods, as they are properly called) are POST, GET, PUT, PATCH, and DELETE. These correspond to create, read, update, and delete (or CRUD) operation.

| HTTP Verb        | CRUD           | Entire Collection (e.g. /customers)  | Specific Item (e.g. /customers/{id})
| ---------------- |:--------------:| ------------------------------------:| ------------------------------------:|
| POST      | Create | 201 (Created), 'Location' header with link to /customers/{id} containing new ID. | 404 (Not Found), 409 (Conflict) if resource already exists..
| GET       | Read | 200 (OK), list of customers. Use pagination, sorting and filtering to navigate big lists. | 200 (OK), single customer. 404 (Not Found), if ID not found or invalid.
| PUT  | Update/Replace	 | 405 (Method Not Allowed), unless you want to update/replace every resource in the entire collection. | 200 (OK) or 204 (No Content). 404 (Not Found), if ID not found or invalid.
| PATCH  | Update/Modify |405 (Method Not Allowed), unless you want to modify the collection itself. | 	200 (OK) or 204 (No Content). 404 (Not Found), if ID not found or invalid.
| DELETE  | Delete | 405 (Method Not Allowed), unless you want to delete the whole collection—not often desirable. |200 (OK). 404 (Not Found), if ID not found or invalid.

Refs: https://restfulapi.net/http-methods
2. How many HTTP request methods?
-  HTTP defines a set of request methods to indicate the desired action to be performed for a given resource. Although they can also be nouns, these request methods are sometimes referred to as HTTP verbs. Each of them implements a different semantic, but some common features are shared by a group of them: e.g. a request method can be safe, idempotent, or cacheable.

GET
The GET method requests a representation of the specified resource. Requests using GET should only retrieve data.

HEAD
The HEAD method asks for a response identical to a GET request, but without the response body.

POST
The POST method submits an entity to the specified resource, often causing a change in state or side effects on the server.

PUT
The PUT method replaces all current representations of the target resource with the request payload.

DELETE
The DELETE method deletes the specified resource.

CONNECT
The CONNECT method establishes a tunnel to the server identified by the target resource.

OPTIONS
The OPTIONS method describes the communication options for the target resource.

TRACE
The TRACE method performs a message loop-back test along the path to the target resource.

PATCH
The PATCH method applies partial modifications to a resource.

Ref: https://developer.mozilla.org/en-US/docs/Web/HTTP/Methods
