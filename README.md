# HTTP Basic for web developers.

### What is HTTP
- Stands for Hypertext Transfer Protocol
- HTTP is an asymmetric request-response client-server protocol
- Enables communication between clients and servers over the internet. 
- Allow the transferring of data in various formats. IE, videos, images, JSON, HTML and more. 
- HTTP is a stateless protocol. In other words, the current request does not know what has been done in the previous requests.
- HTTP permits negotiating of data type and representation, so as to allow systems to be built independently of the data being transferred.
- Commnunication methods 
  - Request 
  - Response

### HTTP Client 
An HTTP client sends a request message to an HTTP server.
Whenever you issue a URL from your browser to get a web resource using HTTP, for example http://www.google.com, the browser turns the URL into a request message and sends it to the HTTP server. The HTTP server interprets the request message, and returns you an appropriate response message, which is either the resource you requested or an error message

### HTTP Server
HTTP server returns a response message to HTTP client's request. 


### what is URL 
- stands for Uniform Resource Locator 
URL (http//www.google.com:80/images) has for parts 
1. Protocol (https): The application-level protocol used by the client and server, e.g., HTTP, FTP, and telnet.
2. Hostname (www.google.com): The DNS domain name (e.g., www.google.com) or IP address (e.g., 8.8.8.8.4.4) of the server.
3. Port (80): The TCP port number that the server is listening for incoming requests from the clients.
4. Path-and-file-name (/images): The name and location of the requested resource, under the server document base directory.


### Types of request 
- GET - to fetch one or more records of data from server
- POST - to create new records
- PUT - to update one or more records of data
- PATCH - to update one or partial of a reocrd of data
- DELETE - to remove a specific record of data
- ...

## HTTP Request Message
Every HTTP request has two below parts
1. Request Message Header (required)
2. Request Message body (optional)

### Request Message Header 
It has two parts 
#### 1. Request Line
It has 3 parts 
- request method: get, post, put, patch...
- request URI: www.domain.com/user/23/update
- HTTP version 1.0 or 1.1
```
UPDATE /user/23/update.html
```
#### 2. Request Headers
The request headers are in the form of name:value pairs. Multiple values, separated by commas, can be specified.
```
Host: www.domain.com
Connection: Keep-Alive
Accept: image/gif, image/jpeg, */*
Accept-Language: us-en, fr, cn
```

## HTTP Response Message
Consist of two parts
1. Response Message Header (required)
2. Response Message body (optional)

### Response Message Header 
It has two parts 
#### 1. Stutus Line
- syntax: HTTP-version status-code reason-phrase 
- HTTP-version: http/1.0 and http/1.1 
- status-code: 3-digit number generate by server reflects response. (200, 404, 403, 500)
- reason-phrase: short explanation to status code. "OK", "403", "500"
- Common status code and reason phrase: "200 OK", "404 Not Found", "403 Forbidden", "500 Internal Server Error".

##### 3. Response Header (optional)
The response headers are in the form name:value pairs as below: 
``` response-header-name: response-header-value1, response-header-value2, ... ```
Examples of response headers are:
```
Content-Type: text/html
Content-Length: 35
Connection: Keep-Alive
Keep-Alive: timeout=15, max=100
```


