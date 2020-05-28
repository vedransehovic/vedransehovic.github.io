---
layout: post
title:      "Understanding APIs"
date:       2020-05-28 23:18:05 +0000
permalink:  understanding_apis
---

![](https://www.computerhope.com/cdn/linux/curl.gif)

This blog post came about in relation to the Flatiron's CLI Project I was working on during last week. Everything in the project was, more or less, summation of the course material learned in prior 6 weeks (of part time course.) Everything but REST API. Sure we knew how to get the data from an API but it was a black box. "You isntall this gem and type these commands and data magically appears." That is fine and has gotten me through the project but now that I have some time it would be fun to lift the hood a little bit and explore the process behind it. 
Starting from a definition. REST stands for "Representational State Transfer" and API stands for "Applicaton Programming Interface." REST is basically a set of rules that developers follow when they create their APIs (points at which others can interact with their programs.)
Basic feature of REST APIs is what we used in this project. A request that is made up of 4 things: 

1. Endpoint
2. The method
3. The headers
4. The data (body)

Root - endpoint is the starting point of the API and it's followed by the path. Good explanation of this is that root is the auto attendant and path(s) are different extensions you can choose from. I have personally came across this when I had to implement 2 different API calls to get the seperate but connected pieces of information needed for the project. 
The Method - is the type of request sent to the server. Types are:

- GET
- POST
- PUT
- PATCH
- DELETE

I suspected there must be other methods than just the one we used for this project. GET will gets you the data, POST is used to create a new resource on the server, PUT and PATCH are used to update resource on a server and DELETE is too self explanatory to mention. 

But how do we manipulate these methods, I know how to get the data out but how would I try to put data in the API's database (if I had access to it.) Enter cURL.
cURL
cURL is a command line utility used to check, test and use APIs. For the project I've tested my connections in the browser and that worked fine, but it would've been much more efficient if I knew about cURL beforehand. CURL commands work in the following fashion:

curl -X <method> <root-url><path>

So to get data out we would type: curl -X GET https://whateverurl.com/path
and to post data we would type: curl - X POST https://whateverurl.com/path

The Headers are used to provide information to both client and the server. They can be used in multiple ways, for example authentication and providing information about the actual body content. Important information is that headers are property-value pairs seperated by colon. Good example would be: 

"Content-type: application/json"

Above example of a header is telling us to expect the body in json format, really popular delivery format for APIs (none of the API's that I've came across in my research for this project was delivered in anything but JSON)

The Data or body contains information portion of your API request and it's needed to be specified only on Post or update requests. On GET request it's pulled automatically and addressed as "data"
This is only a scratch below the surface as far as anatomy of API is concerned but it really helped me understand it and not treat it as a black box. Plenty of things to learn such as authentication protocol, API versioning etc. but it doesn't seem very daunting to learn. 






