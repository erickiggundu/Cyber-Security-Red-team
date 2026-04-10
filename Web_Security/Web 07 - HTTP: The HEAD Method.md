#URL/Link
https://training.olicyber.it/challenges

#Catergory
Web Security

#Description
Sometimes, a client may want to know the metadata of a resource without necessarily receiving the entire representation 
(think, for example, of a large file). For these specific situations, the HTTP protocol provides the HEAD verb, designed to obtain the headers of an equivalent GET request in response, but without actually transferring the resource.
The headers shown should be identical to those of a similar GET request, but as with the header Accept, a faulty or misconfigured server can accidentally leak additional information that would not be included in the response to a 
normal GET request.
The goal of this challenge is to make a HEAD request to the resource http://web-07.challs.olicyber.it/and observe the returned headers. 
It is recommended to use the library's headrequests function , which has similar uses to the get.

#Method_of_Solve:
So we started by pasting the our token to and then we loaded and showed (unauthorized) after that i looked into the web developer tools and i looked @ the cookes
after i checked into the cookies and loaded the Network panel and i right clicked on seen the Get link and i changed to the headers and the i sent the request and went down and see the flag in the x section 
#Another Option:
you can use curl:

curl -I http://web-07.challs.olicyber.it/
HTTP/1.1 401 Unauthorized
Content-Length: 12
Content-Type: text/plain; charset=utf-8
Date: Fri, 10 Apr 2026 08:27:02 GMT
Server: nginx/1.21.6
X-Flag: flag{r0gu3_m374d474}
