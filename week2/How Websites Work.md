Web Fundamentals & Security Basics – Learning Summary
🔗 TryHackMe Room: How Websites Work

This document summarizes the key concepts and practical skills I gained while completing a beginner-friendly room on how websites function, how front-end technologies work, and how basic web vulnerabilities are introduced and exploited.

Task 1: How Websites Work
Websites are made of two main components:

Front End (Client-Side): What the user sees and interacts with in the browser.

Back End (Server-Side): Handles user requests, logic, and data processing.

When you visit a website, your browser sends a request to a web server, and the server sends back the necessary data to display the page.

A web server is essentially a remote computer designed to respond to these kinds of requests.

Task 2: HTML
HTML (HyperText Markup Language) is used to build the structure of web pages.

Core elements:

<!DOCTYPE html>: Declares the use of HTML5.

<html>, <head>, <body>: Define the document’s overall structure.

<h1>, <p>, <img>, <button>: Common content tags.

HTML attributes:

class: Used for styling multiple elements similarly.

id: A unique identifier for individual elements (useful in CSS and JS).

src: Specifies the source of an image (<img src="...">).

You can view the source code of any webpage using “View Page Source” in your browser.

Task 3: JavaScript
JavaScript (JS) enables interaction and real-time functionality on web pages.

Without JS, pages are static and non-interactive.

JS can be added:

Inline using <script> tags.

Externally using src attributes (e.g., <script src="..."></script>).

Example:

js
Copy
Edit
document.getElementById("demo").innerHTML = "Hack the Planet";
You can also add events like onclick to trigger code when users interact:

html
Copy
Edit
<button onclick='document.getElementById("demo").innerHTML = "Button Clicked";'>Click Me!</button>
task 4: Sensitive Data Exposure
Sometimes, developers accidentally leave sensitive information in the HTML or JavaScript source code.

Common examples:

Hardcoded test passwords (e.g., <!-- password: testpasswd -->)

Hidden links to private or admin sections

Always inspect the page source when testing a site — you might find exposed credentials or access points.

Task 5: HTML Injection
HTML Injection happens when user input is displayed on the page without proper sanitization.

This allows attackers to inject their own HTML or even JavaScript into the page.

Example attack:

html
Copy
Edit
<a href="http://hacker.com">Click me</a>
To prevent this, all user input must be sanitized before being rendered.

What I Learned
Clear understanding of how websites work from front to back.

Gained foundational knowledge of:

HTML (structure)

CSS (styling, briefly)

JavaScript (behavior & interaction)

Learned about basic web vulnerabilities:

Sensitive Data Exposure

HTML Injection

Improved skills in:

Viewing and analyzing web page source code

Writing and reading HTML and JavaScript

Recognizing common security oversights

Reinforced the golden rule of web development:
"Never trust user input!" – Always sanitize and validate it.