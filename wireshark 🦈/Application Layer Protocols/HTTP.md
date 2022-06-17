Data on the web is transferred using the HTTP/HTTPS application layer protocol. Normal communication in #HTTP follows a request/response model, where the communication between a client and a server is coordinated by a set of rules. The client requests for a certain resource to the server and then receives a status code that specifies the current status of the requested resource. If available then, the resource is also sent along with the status code, else the client would receive a not-available status code.

**How request/response work?**
Web servers utilize HTTP to serve web pages to the requesting clients. At the beginning of every HTTP session, the *TCP three-way handshake takes place*. It creates a dedicated channel between the communicating hosts followed by HTTP and data packets, which are sent in and received while the session is active.

![[Pasted image 20220606200537.png]]
- In the first line, there are three things passed on to the server as the arguments, which are the HTTP method, the requested resource, and the location / (root directory). 
- The Host argument is required by the HTTP/1.1 protocol requests. The value of this field is the web server’s address that you typed in the address bar of the browser. The ACCEPT parameter specifies what kind of content is acceptable by the requesting client response.
-  The If-modified-since parameter is sent from the client to the server, which includes the date and time of your previous request made to the server. If the server contents have been changed since your previous request, then you will receive the new updated page. Otherwise, your system will present you with the locally cached page. 
- The user-agent specifies the browser-related information that you are using. This information is to be used by the server to present you with browser-compatible content. Parameters such as Accept-Language and Accept-Encoding are passed on to the server to inform us of what type of content is acceptable to the client. 
- The Connection-alive parameter specifies whether the client wishes to keep the connection working after this particular request has been processed.


