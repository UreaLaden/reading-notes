# Object-Oriented Programming Concepts
## [Home](../Readme.md)

### Objects: A software bundle of related state and behavior, often used to model real world objects.
Real-world objects share two characteristics: They all have **state** and **behavior**. Dogs have state(`name`,`color`,`breed`,`hungry`)
and behavior(`barking`,`fetching`,`wagging tail`). Bicycles also have state (`current gear`, `current pedal cadence`, `current speed`) and behavior
(`changing gear`,`changing pedal cadence`,`applying brakes`)
### Class: A blueprint or prototype from which objects are created.
In the real world, you'll often find many individual objects all of the same kind. There may be thousands of other bicycles in existence, all of the same
make and model. Each bicycle was built from the same set of blueprints and therefore contains the same components. In obect-oriented terms, we say that your
bicycle is an *instance* of the *class of objects* known as bicycles.
```
class Bicycle {

    int cadence = 0;
    int speed = 0;
    int gear = 1;

    void changeCadence(int newValue) {
         cadence = newValue;
    }

    void changeGear(int newValue) {
         gear = newValue;
    }

    void speedUp(int increment) {
         speed = speed + increment;   
    }

    void applyBrakes(int decrement) {
         speed = speed - decrement;
    }

    void printStates() {
         System.out.println("cadence:" +
             cadence + " speed:" + 
             speed + " gear:" + gear);
    }
}
```
### Inheritance: Provides a powerful and natural mechanism for organizing and structuring your software.
Object-oriented programming allows classes to inherit commonly used state and behavior from other classes. In this example, Bicycle now becomes the superclass of MountainBike, RoadBike, and TandemBike.
### Interface: A contract between a class and the outside world. When a class implements an interface, it promises to provide the behavior published by that interface.
In its most common form, an interface iws a group of related methods with empty bodies. A bicycle's behavior,
if specified as an interface, might appear as follows:
```
interface Bicycle {

    //  wheel revolutions per minute
    void changeCadence(int newValue);

    void changeGear(int newValue);

    void speedUp(int increment);

    void applyBrakes(int decrement);
}
```
To implement this interfact, the name of the class would change (to a particular brand of bicycle),and we'd use the `implements` keyword in the class declaration.
```
class ACMEBicycle implements Bicycle {

    int cadence = 0;
    int speed = 0;
    int gear = 1;

   // The compiler will now require that methods
   // changeCadence, changeGear, speedUp, and applyBrakes
   // all be implemented. Compilation will fail if those
   // methods are missing from this class.

    void changeCadence(int newValue) {
         cadence = newValue;
    }

    void changeGear(int newValue) {
         gear = newValue;
    }

    void speedUp(int increment) {
         speed = speed + increment;   
    }

    void applyBrakes(int decrement) {
         speed = speed - decrement;
    }

    void printStates() {
         System.out.println("cadence:" +
             cadence + " speed:" + 
             speed + " gear:" + gear);
    }
}
```
### Package: A namespace for organizing classes and interfaces in a logical manner. Placing code into packages makes large software projects easier to manage. 
The Java platform provides an enormous class library (a set of packages) suitable for use in your own applications. This library is known as the "Application Programming Interface", or "API" for short. Its packages represent the tasks most commonly associated with general-purpose programming. For example, a String object contains state and behavior for character strings; a File object allows a programmer to easily create, delete, inspect, compare, or modify a file on the filesystem; a Socket object allows for the creation and use of network sockets; various GUI objects control buttons and checkboxes and anything else related to graphical user interfaces.




## Sources
## [The Java Tutorials](https://docs.oracle.com/javase/tutorial/java/concepts/)