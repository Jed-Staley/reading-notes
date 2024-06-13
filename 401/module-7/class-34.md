# Class 34 Reading Notes

## Introduction

This reading covers the differences between query string parameters and path parameters, building a dynamic API interface, and implementing authentication and authorization using middleware. It also explains the OAuth handshake and Role Based Access Control (RBAC).

## Notes

### Explain the difference between a query string parameter and a path parameter

- **Query String Parameter**: These parameters are appended to the end of a URL after a question mark (`?`). They are used to filter or sort resources. For example, `http://example.com/items?type=book`.
- **Path Parameter**: These parameters are part of the URL path itself and are used to identify specific resources. For example, `http://example.com/items/123` where `123` is the path parameter.

### What would our API URL with a path id parameter be given the following information

- **Domain**: <http://our-site.com>
- **Version**: v3
- **Model name**: stuff
- **ID**: things

API URL: `http://our-site.com/v3/stuff/things`

### We have created a dynamic API with an “interface”. Describe how that interface works to a non-technical friend

Imagine the API interface as a menu in a restaurant. Instead of telling the chef exactly how to cook each dish, you just pick what you want from the menu. The API interface works similarly; it provides a list of options (endpoints) you can interact with. Each endpoint lets you request specific data or perform certain actions without needing to know the complex details behind the scenes.

### Describe how you would use middleware to implement basic and bearer auth

- **Basic Auth Middleware**: This middleware checks the `Authorization` header for a username and password encoded in Base64. It decodes and verifies the credentials before granting access to the requested resource.
  
  Example:

  ```javascript
  function basicAuth(req, res, next) {
    const authHeader = req.headers.authorization;
    if (!authHeader) {
      return res.status(401).send('Missing Authorization header');
    }
    const encoded = authHeader.split(' ')[1];
    const decoded = Buffer.from(encoded, 'base64').toString('ascii');
    const [username, password] = decoded.split(':');
    if (verifyCredentials(username, password)) {
      next();
    } else {
      res.status(401).send('Invalid credentials');
    }
  }
  ```

- **Bearer Auth Middleware**: This middleware checks the `Authorization` header for a Bearer token. It verifies the token's validity and extracts user information to authorize access to the resource.
  
  Example:

  ```javascript
  function bearerAuth(req, res, next) {
    const authHeader = req.headers.authorization;
    if (!authHeader) {
      return res.status(401).send('Missing Authorization header');
    }
    const token = authHeader.split(' ')[1];
    if (verifyToken(token)) {
      req.user = decodeToken(token);
      next();
    } else {
      res.status(401).send('Invalid token');
    }
  }
  ```

### Describe the handshake necessary to implement OAuth

The OAuth handshake involves several steps:

1. **Authorization Request**: The client requests authorization from the resource owner via the authorization server.
2. **Authorization Grant**: The resource owner grants authorization, typically by logging in and consenting to the requested permissions.
3. **Access Token Request**: The client exchanges the authorization grant for an access token from the authorization server.
4. **Access Token Response**: The authorization server returns an access token, which the client can use to access protected resources.

### Describe how Role Based Access Control works to a non-technical friend

Role Based Access Control (RBAC) works like a keycard system in a building. Different people have different keycards that grant them access to specific rooms based on their roles. For example, an admin keycard might open every door, while an employee keycard only opens certain office doors. In software, RBAC assigns permissions to roles, and users are given roles that determine what they can access or do within the system.

## Reflection

### What are your learning goals after reading and reviewing the class README?

My learning goals include understanding the differences between query string and path parameters, mastering the implementation of dynamic API interfaces, and effectively using middleware for authentication and authorization. Additionally, I aim to grasp the OAuth handshake process and the principles of Role Based Access Control (RBAC).
