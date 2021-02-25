# Notes on Functional Programming 

##### Definition
Functional programming is a a style of building the structure and elements of computer programs that treats computation as the evaluation of mathematical functions and avoids changing-state and mutable data. 

##### Pure Functions
These functions return the same result if given the same arguments and do not cause any observable side effects.**If the function reads external files it's not a pure function**.

##### Impure Functions
The functions use global objects not passed as parameters. Any function that relies on a random number generator cannot be pure.  

The benefits to using pure functions lie in the ease of testing. 

A simple example would be a function to receive a collection of numbers and expect it to increment each element of this collection. We receive the numbers array, use map incrementing each number, and return a new list of incremented numbers.

For the input ```[1, 2, 3, 4, 5]```, the expected output would be ```[2, 3, 4, 5, 6]```.

##### Immutable data
The state of this type of data cannot change after it has been created. Since we can't change this immutable object, our only option is to **create a new object with a new value**. In Javascript we commonly use the for loop. This next for statement has some mutable variables.For each iteration, we are changing the i and the sumOfValue state. The way to handle mutability in iteration is through recursion.

So here we have the sum function that receives a vector of numerical values. The function calls itself until we get the list empty (our recursion base case). For each "iteration" we will add the value to the total accumulator.
With recursion, we keep our variables immutable. The list and the accumulator variables are not changed. It keeps the same value.

##### Referential Transparency

This pure function will always have the same output, given the same input. Passing 2 as a parameter of the ```square function``` will always returns 4. So now we can replace the `square(2)` with 4. That's it! Our function is `referentially transparent`.

`purefunctions + immutable data = referential transparency`



## Source: [TK: Concepts of Functional Programming in Javascript](https://medium.com/the-renaissance-developer/concepts-of-functional-programming-in-javascript-6bc84220d2aa)
