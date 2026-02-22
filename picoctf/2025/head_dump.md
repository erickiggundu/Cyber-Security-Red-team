#Url/Link:
https://play.picoctf.org/practice/challenge/476?
#Category: 
*Web Exploitation
#Description:
*Welcome to the challenge! In this challenge, you will explore a web application and find an endpoint that exposes a file containing a hidden flag.
*The application is a simple blog website where you can read articles about various topics, including an article about API Documentation. Your goal is to explore the application and find the endpoint that generates files holding the server’s memory, where a secret flag is hidden.
*Additional details will be available after launching your challenge instance.
#Challenge:
*picoCTF News - Heap Dump Exposure
#Method Of Solving 
A blog website built on Node.js accidentally exposes a /heapdump endpoint that dumps the server's RAM memory. The flag is stored in memory as a plain text variable and can be extracted from the dump.

Steps
Step 1 — Visit the website
Browse to the challenge URL and read the blog articles. One article hints at backend development with #swagger UI and links to /api-docs.
Step 2 — Discover the endpoint
bashcurl -s http://<url>/ | grep -i "heap\|dump\|backend\|api\|endpoint"
This reveals a link to /api-docs and mentions Swagger UI.
Step 3 — Download and search the heap dump
bashcurl -s http://<url>/heapdump | strings | grep -oP 'picoCTF\{[^}]+\}'
```

**Step 4 — Flag retrieved**
