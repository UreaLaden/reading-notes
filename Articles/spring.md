# Spring MVC and Thymeleaf

[Home](../Readme.md)

In a typical Spring MVC application, `@Controller` classes are responsible for preparing a model 
map with data and selecting a view to be renered. This model map allows for the complete 
abstraction of the view technology and, in the case of Thymeleaf, it is transformed in to a 
Thymeleaf context object that makes all the defined variables available to expressions executed 
in templates.

Spring MVC calls the piece of data that can be accessed during the execution of views model 
attributes commonly referred to in Thymeleaf language as *context variables*.

There are several ways of adding model attributes to a view in Spring MVC:

1. Add attribute to `Model` via its `addAttribute` method.
2. Return `ModelAndView` with model attributes included.
2. Expose common attributes via methods annotated with `@ModelAttribute`

To access url parameters, there are also several methods.

1. Use the `param.` prefix.

![Spring1](../img/spring1.png)

2. Since parameters can be multivalued (e.g. `https://example.com/query?q=Thymeleaf%20Is%20Great!
   &q=Really%3F`) you may access them using brackets syntax 

![Spring1](../img/spring2.png)

3. by using the special `#request` object that gives you direct access to the `javax.servlet.http.
   HttpServletRequest` object  

![Spring1](../img/spring3.png)


## Source
[Rafat Borowiec](https://www.thymeleaf.org/doc/articles/springmvcaccessdata.html)