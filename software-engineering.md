### Object Oriented Programming
---
##### Abstraction 
```
hide all but important features to reduce complexity and think about things at a higher level

ex) create an object TV to focus on a higher level, rather than the specifics/internals of a TV
``` 

##### Encapsulation 
```
bundling data fields as private to prevent open access and change  
```

##### Inheritance
```
parent class : Dog 
child class : Retriever 

child class can inherit all data fields and methods of parent class, while defining its own fields or methods 

Advantages : 
  1) Reusability : Do not have to write already existing lines of code 
```

##### Polymorphism
```
Triangle shape = new Triangle() 
Shape shape = new Triangle()           class triangle is a part of class shape
Shape shape = new Circle()             class circle is a part of class shape 
Triangle shape = new Shape()           a triangle is a shape, but a shape is not a triangle (invalid)

public void run(Shape shape) {}        classes shape, triangle, and circle can all be passed to the parameter

Advantages :
  1) Flexibility 
```

##### Composition 
```
defines a has-a relationship
public class Point3D {
  public Point3D(int x, int y, int z) {
    p = new Point2D(x,y);
  }
}
```

##### Dependency Injection 
```
Suppose you have a class that depends on another object 

public Car() {
  Wheel wheel = new CanadianWheel();
  Windows window = new CanadianWindow();
}

Wheel and windows are 'dependencies' of car because they are needed to construct the car 

What if we want to create multiple objects of car, but with different wheels, companies, and materials?

Instead of instantiating and setting dependencies within the class, one can create a dependency from the outside 

This exterior dependency (e.g. wheel) can then be injected into the class car  

public Car(Wheel wh, Windows wi) {
  this.wheel = wh;
  this.windows = wi;
}

Advantages :
  1) Makes testing easier as dependency classes do not have to be instantiated 
  2) Allows for independent development of classes 
  3) Can easily switch out different dependencies to the class 
  4) Can use the dependencies in other classes 
```

##### Object Relational Mapping
```
Converting data between relational databases and OOP languages such that they become compatible with each other
Query database using an object-oriented paradigm (graph of objects) instead of SQL (tabular format) 
```

<br />

### Terms in Software Engineering 
---
##### Languages 
```
compiled language : compiler translates program to machine code before execution, time needed to compile every time changes are made, fast during runtime 
interpreted language : interpreter reads and executes program without compilation, dynamic typing, smaller memory size, slow during runtime   

strong typing : interpreter does not allow operations with incompatible types ("1" + 1)
weak typing : interpreter does allow operations with incompatible types ("1" + 1 = 2)

static typing : type is checked during compile time 
dynamic typing : type is checked during runtime
```

##### Programming Paradigms 
```
declarative programming : tell program specifically what you want it to do (this is A, this is B made from A, return C made from B)
imperative programming : tell program how you would like it to do something (this is A, we will go through this loop, we check this, if B, return A)

functional programming :
  1) paradigm where programs are composed of functions that are independent of outside states 
    ex) x = 5 
        func double():  
          x *= 2        // changes the state of an outside variable 
          return x  

        instead, 
        func double(num):
          return num * 2  // does not change outside variables 
  2) does not share states 
  3) paradigm where functions are treated as "first-class citizens" (can save as variable, pass as argument, be returned)
    ex) func double(func2):
          return func3   
```

##### Terms 
```
Web Server : return content of file following HTTP protocols (Apache HTTP)
Application Server : execute and display results of file following various protocols (Oracle WebLogic, Apache Tomcat)

Regression Testing : testing to confirm that recent program change does not impact existing functionality 
Automated Testing : reduce time, cost, and errors by automating certain test cases that are repetitive, tedious, or difficult to test manually
  ex) QTP, Rational Robot, Selenium
```

##### Methodology
```
Agile
  1) approach to break development into stages and constantly collaborate with end users
  2) advocates adaptive planning, evolutionary development, early delivery, and continual improvement 
 
DevOps 
  1) set of practices to reduce the time between committing a change, and the change being placed into production 
  2) integrate development and operations teams to improve collaboration by automating testing, infrastructure, workflows 
 
CI/CD
  1) continous integration, continous delivery 
  2) bridges gap between development and operations through automation to allow DevOps procedures
  
ETL 
  1) extract, transform, and load one database to another
```
