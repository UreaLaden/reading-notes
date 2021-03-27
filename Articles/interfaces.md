# Interfaces in Java
[Home](../Readme.md)
## Definition:  An interface is a reference type, similar to a class, that can contain only 
## constants, method signatures, default methods, static methods, and nested types. 
**Interfaces cannot be instantiated** -- they can only be *mplemented*by classes or*extended*by other interfaces. 

```
public interface OperateCar{
    // constant declarations, if any
    // method signatures
    
    // An enum with values RIGHT, LEFT
    int turn(Direction direction, double radius, double startSpeed, double endSpeed);
    int changeLanes(Direction direction, double startSpeed, double endSpeed);
    int signalTurn(Direction direction, boolean signalOn);
    int getRadarFront(double distanceToCar, double speedOfCar);
    int getRadarRear(double distanceToCar, double speedOfCar);
    
    .......
    //more methods
```

To use an interface, write a class that implements the interface. When instantiate it provides a 
method body for each of the methods declared in the interface.

```
public class OperateBMW implements OperateCar{
    // the OperateCar method signatures, with implementation -- 
    // for example:
    int signalTurn(Direction direction, boolean signalOn){
        // code to turn BMW's LEFT turn indicator lights on 
        // code to turn BMW's LEFT turn indicator lights off 
        // code to turn BMW's RIGHT turn indicator lights on 
        // code to turn BMW's RIGHT turn indicator lights off
    }
    
    // other members, as needed -- for example, helper classes not 
    // visible to clients of the interface 
```
### Source
[Oracle Docs](https://docs.oracle.com/javase/tutorial/java/IandI/createinterface.html)



