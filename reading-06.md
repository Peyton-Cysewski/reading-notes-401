# Interfaces

## Inheritance
- Inherited classes have all the same characteristics of the main class from which the original characteristics come from.
- Base class - The root class from which other classes can inherit their characteristics.
- Derived class - The class that has inherited characteristics and has the ability to extend/add upon them.
- A derived class implicitly inherits all the members of a base class except for its constructors and finalizers. It also reuses the base class' methods without having to reimplement them.

## Abstract
- The ```abstract``` keyword allows for classes and class members to be incomplete, requiring them to be implemented in a derived class.
- The ```virtual``` keyword allows for a method to be written. It can subsequently be overridden by an ```abstract``` method in a derived class. Any class that is then derived from this class will again have access to the original ```virtual``` method, but not the previous overridden definition.
- The ```sealed``` keyword makes a class underivable, meaning it cannot be used as a base class.

## Polymorphism
- At run time, objects of a derived class may be treated as objects of a base class in places such as method parameters and collections or arrays. When this polymorphism occurs, the object's declared type is no longer identical to its run-time type.
- Base classes may define and implement ```virtual``` methods, and derived classes can override them, which means they provide their own definition and implementation. At run-time, when client code calls the method, the CLR looks up the run-time type of the object, and invokes that override of the ```virtual method```. In your source code you can call a method on a base class, and cause a derived class's version of the method to be executed.

## OOP Principles
- Abstraction means hiding the unnecessary details from type consumers.
- Encapsulation means that a group of related properties, methods, and other members are treated as a single unit or object.
- Inheritance describes the ability to create new classes based on an existing class.
- Polymorphism means that you can have multiple classes that can be used interchangeably, even though each class implements the same properties or methods in different ways.
Supported in C#:
- Classes and Objects: Class members, properties and fields, methods, constructors, finalizers, events, nested classes, access modifiers and access levels, statics, anonymous types.
- Inheritance: overriding members.
- Interfaces
- Generics
- Delegates



[Table of Contents](README.md)