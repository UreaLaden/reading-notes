# EJS Partials

[Home](../README.md)

Partials allow you to reuse the same HTML across multiple views. They make large websites easier to maintain as you don’t have to go and change a piece of text in every page it appears in. Instead, you define that reusable bundle of code in a file and include it wherever you need it.

The <%- %> tags allow us to output the unescaped content onto the page (notice the -). This is important when using the include() statement since you don’t want EJS to escape your HTML characters like ‘<’, ‘>’, etc…

[Partials 1](../img/partials_1.png)

Creating and including partials is very straightforward with EJS. 

[Partials 2](../img/partials_2.png)


#### Source:
[Hensle Josephe](https://medium.com/@henslejoseph/ejs-partials-f6f102cb7433)