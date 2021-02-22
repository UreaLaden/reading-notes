# REST

HTTP is a webserver tells browser which protocol to use. A common analogy would be that of GPS coordinates for knowledge and information. The world wide web is built on an architectural style called **REST** which provides a definition of a **resource**. Web pages are representations of these resources, also referred to as concepts.URLs tell the browser that there's a concept somewhere. A browser can go ask for a specific representation of the concept. Specifically, the browser asks for the web page representation of the concept. 

When we go to a web page, the browser does an `HTTP` `GET` on the URL typed in and returns a web page. The web page just specifies the URLs to the images and the browser goes and does more GETs using the `HTTP` protocol on them until all the resources are obtained and the web page is displayed. But the important thing here is that very different kinds of nouns can be treated the same. Whether the noun is an image, text, video, an mp3, a slideshow, whatever. I can `GET` all of those things the same way given a URL. If one system needs to add something to another system, it would use an `HTTP` `POST`. If a system wants to replace something in another system, it uses an `HTTP` `PUT`, or, to do a partial update, it'll hopefully use `PATCH`. 

[Ryan Tomayko: How I explained REST to my Brother](https://gist.github.com/brookr/5977550)
