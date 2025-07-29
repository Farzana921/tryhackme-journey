# HTTP Basics — TryHackMe Summary

This document summarizes the core concepts and lessons I gained from completing the **HTTP Basics** room on TryHackMe. It covers the essentials of how HTTP works and how data travels between clients and servers on the web.



## What I Learned

Throughout the tasks, I built a strong foundation in understanding:

- The difference between HTTP and HTTPS and their purposes
- The structure and role of URLs in web requests
- How different HTTP methods (GET, POST, PUT, DELETE) are used to interact with web servers
- The meaning behind various HTTP status codes and how they inform client-server communication
- The use of headers to send extra information in requests and responses
- How cookies maintain sessions and enable user authentication
- How to craft and execute different types of HTTP requests in practice



## Breakdown

## Task 1: Understanding HTTP and HTTPS
- HTTP is the protocol for requesting and transferring webpage data.
- HTTPS is the secure, encrypted version ensuring data privacy and server authenticity.
- **Flag found:** `THM{INVALID_HTTP_CERT}`


## Exploring Requests and Responses
- A URL is a web address made up of several parts: scheme, user info, host, port, path, query, and fragment.
- HTTP requests start with a method line and include headers for additional data.
- HTTP responses include a status line, headers, and the requested content.



## HTTP Methods Overview
- **GET** to retrieve information.
- **POST** to submit new data.
- **PUT** to update existing data.
- **DELETE** to remove data.



## HTTP Status Codes Explained
- Status codes are grouped by category:
  - 1xx: Informational messages
  - 2xx: Successful responses (e.g., 200 OK, 201 Created)
  - 3xx: Redirects
  - 4xx: Client errors (e.g., 401 Unauthorized, 404 Not Found)
  - 5xx: Server errors (e.g., 500 Internal Server Error, 503 Service Unavailable)



## HTTP Headers Deep Dive
- **Request Headers** like `Host`, `User-Agent`, and `Content-Length` provide context about the client and request.
- **Response Headers** such as `Set-Cookie`, `Content-Type`, and `Cache-Control` deliver metadata about the response.



## Understanding Cookies
- Cookies are small pieces of data stored on the client to maintain state and session information.
- They are set by servers via the `Set-Cookie` header and sent back with requests in the `Cookie` header.



## Practical HTTP Requests
- Successfully performed requests using different HTTP methods, receiving corresponding challenge flags:
  - `GET /room` → `THM{YOU'RE_IN_THE_ROOM}`
  - `GET /blog?id=1` → `THM{YOU_FOUND_THE_BLOG}`
  - `DELETE /user/1` → `THM{USER_IS_DELETED}`
  - `PUT /user/2` with `username=admin` → `THM{USER_HAS_UPDATED}`
  - `POST /login` with `username=thm` and `password=letmein` → `THM{HTTP_REQUEST_MASTER}`



## Conclusion

Completing this room strengthened my understanding of the HTTP protocol and the mechanics of web communication. These fundamentals are essential for web development, debugging, and cybersecurity tasks such as penetration testing. This knowledge will serve as a solid foundation for deeper exploration into web technologies and security.



*Completed via [TryHackMe - HTTP Basics](https://tryhackme.com/room/httpindetail)*
