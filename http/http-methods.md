# HTTP methods
The Hypertext Transfer Protocol (HTTP) is designed to enable communications between clients and servers.

HTTP works as a request-response protocol between a client and server.

Example: A client (browser) sends an HTTP request to the server; then the server returns a response to the client. The response contains status information about the request and may also contain the requested content.

## GET
GET is used to request data from a specified resource.

Note that the query string (name/value pairs) is sent in the URL of a GET request:

```
    /test/demo_form.php?name1=value1&name2=value2
```

- **GET** requests can be cached
- **GET** requests remain in the browser history
- **GET** requests can be bookmarked
- **GET** requests should never be used when dealing with sensitive data
- **GET** requests have length restrictions
- **GET** requests are only used to request data (not modify)

## POST
POST is used to send data to a server to create/update a resource.

The data sent to the server with POST is stored in the request body of the HTTP request:

```
    POST /test/demo_form.php HTTP/1.1
    Host: w3schools.com

    name1=value1&name2=value2
```

- **POST** requests are never cached
- **POST** requests do not remain in the browser history
- **POST** requests cannot be bookmarked
- **POST** requests have no restrictions on data length

## PUT
PUT is used to send data to a server to create/update a resource.

The difference between POST and PUT is that PUT requests are idempotent. That is, calling the same PUT request multiple times will always produce the same result. In contrast, calling a POST request repeatedly have side effects of creating the same resource multiple times.

## DELETE
The DELETE method deletes the specified resource.

## HEAD
HEAD is almost identical to GET, but without the response body.

In other words, if GET /users returns a list of users, then HEAD /users will make the same request but will not return the list of users.

HEAD requests are useful for checking what a GET request will return before actually making a GET request - like before downloading a large file or response body.