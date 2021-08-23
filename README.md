SOLID PRINCIPLE

S - SINGLE RESPOSIBILITY 
O - OPEN/CLOSE, OPEN FOR EXTENSION CLOSE FOR MODIFICATION
L - LISKOV ( EVERY SUB CLASS OF SUPER CLASS SOULD BEHAVE SAME WHEN IT METHOD CALL/SHOULD NOT BREAK, if S is a subtype of T, then objects of type T may be replaced with objects of type S )
I - INTERFACE SEGREGATION ( A client should never be forced to implement or depend on an interface/method that it doesn't use )
D - DEPENDENCY INVERSION





Liskov Substitutability is a principle in object-oriented programming stating that, in a computer program, if S is a subtype of T, then objects of type T may be replaced with objects of type S

Let's do a simple example in Java:

Bad example
```Javascript
public class Bird{
    public void fly(){}
}
public class Duck extends Bird{}
```

The duck can fly because it is a bird, but what about this:

public class Ostrich extends Bird{}
Ostrich is a bird, but it can't fly, Ostrich class is a subtype of class Bird, but it shouldn't be able to use the fly method, that means we are breaking the LSP principle.

Good example
```Javascript
public class Bird{}
public class FlyingBirds extends Bird{
    public void fly(){}
}
public class Duck extends FlyingBirds{}
public class Ostrich extends Bird{} 
```
