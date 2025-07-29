# Web Fundamentals - HTTP Basics (TryHackMe Summary)

This document summarizes the key concepts and learnings from completing the **"HTTP Basics"** room on TryHackMe. It covers the fundamentals of how web communication works using the HTTP protocol.



## What I Learned

Throughout these tasks, I developed a foundational understanding of how the web works behind the scenes. Key learnings include:

- The role of HTTP/HTTPS in data transmission
- How URLs are structured and interpreted
- The use of HTTP methods (GET, POST, PUT, DELETE)
- Meaning and usage of HTTP status codes
- The importance of HTTP headers and how they are used
- How cookies are used for stateful sessions
- How to construct and test various types of HTTP requests



## Task-by-Task Summary

## Task 1: What is HTTP(S)?
- **HTTP (HyperText Transfer Protocol)** is the protocol for communication between web clients and servers.
- **HTTPS** adds a layer of security using encryption.
- **Challenge Flag:** `THM{INVALID_HTTP_CERT}`


## Task 2: Requests and Responses
- A **URL** includes components like scheme, host, port, path, query string, and fragment.
- HTTP requests contain a method line and headers.
- HTTP responses return a status line, headers, and content.
-  **Headers:** `Host`, `User-Agent`, `Content-Length`, `Content-Type`



## Task 3: HTTP Methods
- **GET** – Retrieve data (e.g., view articles)
- **POST** – Submit new data (e.g., register a user)
- **PUT** – Update existing data (e.g., change settings)
- **DELETE** – Remove data (e.g., delete uploads)


## Task 4: HTTP Status Codes
- Codes are grouped by type:
  - `1xx`: Informational
  - `2xx`: Success (`200 OK`, `201 Created`)
  - `3xx`: Redirection (`301`, `302`)
  - `4xx`: Client Errors (`400`, `401`, `403`, `404`)
  - `5xx`: Server Errors (`500`, `503`)



## Task 5: Headers
- **Request Headers**: `Host`, `User-Agent`, `Content-Length`, `Accept-Encoding`, `Cookie`
- **Response Headers**: `Set-Cookie`, `Cache-Control`, `Content-Type`, `Content-Encoding`



# Task 6: Cookies
- Cookies store session data and are used for authentication.
- Sent using `Set-Cookie` in the response, then sent back via `Cookie` in requests.



## Task 7: Making Requests (Hands-On)
Performed different HTTP requests in an emulator:
-  `GET /room` → `THM{YOU'RE_IN_THE_ROOM}`
-  `GET /blog?id=1` → `THM{YOU_FOUND_THE_BLOG}`
-  `DELETE /user/1` → `THM{USER_IS_DELETED}`
-  `PUT /user/2` with `username=admin` → `THM{USER_HAS_UPDATED}`
-  `POST /login` with `username=thm` and `password=letmein` → `THM{HTTP_REQUEST_MASTER}`



## Final Thoughts

This room gave me a solid grasp of how HTTP powers the web. From basic requests to understanding status codes and headers, these concepts are critical for both web developers and cybersecurity professionals. This knowledge lays a strong foundation for deeper topics like API interaction, web security, and penetration testing.



*Completed via [TryHackMe - HTTP Basics](https://tryhackme.com/room/httpindetail)*
