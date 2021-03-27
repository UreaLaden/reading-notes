# Object Oriented Design
[Home](../Readme.md)
# Solid Principles
SOLID is an acronym for the first five object-oriented design (OOD) principles by Robert C. Martin.
The principles establish practices that lend to developing software with considerations for 
maintaining and extending as the project grows. Adopting these practices can also contribute to 
avoiding code smells, refactoring code, and Agile or Adaptive software development.

# S : Single Responsibility principle (SRP)
#### A class or module should do one thing only and should have only one reason to change.
# O : Open / Closed principle
#### Code entities should be open for extension, but closed for modification. You should write a 
#### class that is closed for modification, but can be extended by, for instance, inheriting from it 
#### and overriding or extending certain behavior.
# L : Liskov Substitution principle (LSP)
#### Any child type of a parent type should be able to stand in for that parent without things blowing
#### up. If you have a class, animal, with a makenoise() method, then any subclass of animal should 
### be able to implement makenoise()
# I : Interface segregation principle(ISP)
#### You should favor many, smaller, client-specific interfaces over on larger, monolithic interface.
# D : Dependency Inversion principle (DIP)
#### Write code that depends upon abstractions rather than upon concrete details. 
-   **Abstraction** : The process of making something easier to understand by ignoring some of 
    the details that may be unimportant. For example: If you're giving your friends directions 
    to your house. You wouldn't describe every house on the street, just that there are 3 houses 
    on the street and yours is the last one.
    
