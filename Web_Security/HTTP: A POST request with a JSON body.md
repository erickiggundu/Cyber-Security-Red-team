#Url/link
https://training.olicyber.it/challenges#challenge-348

#Description
application/x-www-form-urlencoded, despite its historical diffusion, is an obsolete format and not very suitable for representing structured data, which is why it has been gradually supplanted,
in those applications that do not require compatibility with the traditional web form submission mechanism, 
by more modern formats such as XMLand JSON.

The latter, in particular, by virtue of its ease of use in JavaScript, the most widespread web programming language,
has quickly established itself as the new de-facto standard, so libraries like requestsoffer shortcuts for sending POST requests with body encoded in JSONas easily as the old system, as well as for automatically decoding any resources returned in that format by the server in responses.
Similar to the previous one, the goal of this challenge is to send a POST request to the resource, 
http://web-09.challs.olicyber.it/loginproviding JSON the "username": "admin" and "password": "admin" values ​​in the format, 
similar to a hypothetical login operation against a web service. The flag will be returned in the response text.

#Category
Web Security

#Concept
HTTP POST — sending data to a server
JSON encoding — formatting data as {"key": "value"}
Content-Type negotiation — telling the server what format the body is in

#Method Of Solving

so i have used the web Developer Tools where by that used the network panel console log to put the fetching line of code that throwed me the flag as response 
but still i manipulated it using the challenge link of login to Make the Method:POST and then the headers:{"Content-Type":"application/json"}, then body as body:'{"username":"admin","password":"admin"} which accompained 
r=text , then i return and (console.log) and throwed the flag
