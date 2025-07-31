Web Fundamentals Summary

🔗 Room Link: [Red Team Engagements](https://tryhackme.com/room/puttingitalltogether)

This document summarizes key concepts and technologies involved in how the web works, based on a series of modules and tasks I completed. It covers the journey of a web request, the components involved, and various backend and frontend technologies. This is a foundational overview for anyone beginning web development or DevOps.

The Journey of a Web Request
When a user requests a website in their browser, several steps occur behind the scenes:

DNS Resolution – The browser resolves the domain name to an IP address using the Domain Name System (DNS).

HTTP Communication – The browser sends a request using the HTTP protocol to the appropriate web server.

Web Server Response – The server responds with files such as HTML, CSS, JavaScript, and images.

Browser Rendering – The browser processes these files and displays the webpage.

Supporting Web Components
Load Balancers
Distribute incoming traffic across multiple servers to handle high loads and ensure availability.

Use algorithms such as round-robin or least-connections to decide which server to forward requests to.

Perform regular health checks to verify server status.

Automatically stop routing to servers that are unresponsive.

CDN (Content Delivery Network)
Hosts and delivers static files (JavaScript, CSS, images, videos) from globally distributed servers.

Reduces the load on the origin server and minimizes latency by serving content from the closest geographic location.

Databases
Used to store and retrieve user and application data.

Communicate with web servers to provide dynamic content.

Examples include MySQL, PostgreSQL, MongoDB, MSSQL, and others.

WAF (Web Application Firewall)
Sits between the client and the web server.

Protects against common attack types like SQL injection, cross-site scripting, and denial-of-service.

Filters traffic, detects bots, and applies rate limiting to block abusive behavior.

Web Servers
What is a Web Server?
Software that uses HTTP to serve web content to clients.

Common web servers: Apache, Nginx, IIS, NodeJS.

Serve files from a root directory (e.g., /var/www/html on Linux or C:\inetpub\wwwroot on Windows).

Example: A request to http://example.com/picture.jpg serves the file at /var/www/html/picture.jpg.

Virtual Hosts
Allow a single web server to host multiple domain names.

Use HTTP headers to route traffic to the correct website.

Each virtual host can point to a separate directory.

No limit to how many sites can be hosted using virtual hosts.

Static vs Dynamic Content
Static Content: Files that do not change (e.g., HTML, CSS, JS, images).

Dynamic Content: Content that is generated on the fly by the backend (e.g., blog posts, search results).

Dynamic content is processed on the backend and sent to the frontend.

Backend Languages
Handle dynamic functionality and interact with databases or external APIs.

Backend code is not visible to the client.

Common languages: PHP, Python, Ruby, NodeJS, Perl, etc.

Example:

php
Copy
Edit
<html><body>Hello <?php echo $_GET["name"]; ?></body></html>
Requesting index.php?name=adam would return:

html
Copy
Edit
<html><body>Hello adam</body></html>
The PHP code is executed on the server and not visible to the user.

## Key Learnings and Quiz Review


CDNs can be used to host static files and improve content delivery speed.

Load balancers perform health checks to ensure that servers are operational.

WAFs protect websites from hacking attempts and abuse.

Web servers use virtual hosts to host multiple websites.

Dynamic content changes based on logic or user input.

Backend code is not visible to the client browser.

Proper ordering of the request flow reveals the flag: THM{YOU_GOT_THE_ORDER}