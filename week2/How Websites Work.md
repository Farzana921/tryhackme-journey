## Web Fundamentals & Security Basics – Learning Summary

🔗 Room Link: [Red Team Engagements](https://tryhackme.com/room/howwebsiteswork)


This summary covers the key concepts and skills I learned while working through a beginner-friendly web and security training room, focusing on how websites work, front-end languages, and basic security vulnerabilities.

Task 1: How Websites Work
Websites consist of a Front End (client-side) and a Back End (server-side).

The browser sends requests to a web server, which responds with data used to render the page.

The Front End is what the user sees and interacts with; the Back End handles logic, databases, and responses.

Task 2: HTML
HTML (HyperText Markup Language) defines the structure of a webpage.

Key HTML elements:

<!DOCTYPE html>: Declares HTML5.

<html>, <head>, <body>: Main structural tags.

<h1>, <p>, <img>, <button>: Content-specific tags.

HTML elements can have:

class (reusable styling),

id (unique identifier),

src (image source), etc.

You can inspect and view HTML on any site via "View Page Source".

Task 3: JavaScript
JavaScript adds interactivity and dynamic behavior to webpages.

Example use: changing text when a button is clicked.

JS can be embedded inline or via external files using <script> tags.

Events like onclick allow user actions to trigger code.

Example:

js
Copy
Edit
document.getElementById("demo").innerHTML = "Hack the Planet";
Task 4: Sensitive Data Exposure
Websites sometimes expose sensitive data in their source code.

Example vulnerabilities:

Hardcoded passwords in HTML comments.

Hidden admin links.

Always review the page source code when assessing security.

Found password example: testpasswd.

Task 5: HTML Injection
HTML Injection occurs when user input is not sanitized and is directly rendered into the page.

Malicious users can inject HTML or JavaScript to change the page’s structure or behavior.

This is a client-side vulnerability.

Prevent it by sanitizing all user input before rendering.

Example exploit:

html
Copy
Edit
<a href="http://hacker.com">Click me</a>
 What I Gained from These Tasks
Solid understanding of the core technologies that power the web: HTML, CSS, JS.

Awareness of how web requests and responses work.

Learned to identify and exploit basic security issues like:

Sensitive data exposure

HTML injection

Gained hands-on experience in web debugging and inspection tools.

Strengthened understanding of safe coding practices like input sanitization.

