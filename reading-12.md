# Dependency Injection and Repository Design Pattern

## What is Dependency Injection?
A dependency is an object that another object requires. Dependencies can be associated with a class in many different ways, but the most stable way to do so is using interfacing or have the dependency be house in a base class. The framework has a system that takes care of these dependencies that injects the dependency into the object when needed, and disposes it when no longer in use.

## The Repository Pattern
Basically, a repository allows you to populate data in memory that comes from the database in the form of the domain entities. Once the entities are in memory, they can be changed and then persisted back to the database through transactions.
(https://docs.microsoft.com/en-us/dotnet/architecture/microservices/microservice-ddd-cqrs-patterns/infrastructure-persistence-layer-design#the-repository-pattern)

## The SOLID Principles

### Single Responsiblity Principle
Each method should be responsible for exactly one task. One a large scale this makes everything easier. Code is easier to maintain and tests arte easier to write. With tests in mind, it is also a good idea to make tests test for only one use case. All the same reasons apply.
### Open/Close Principle
Any class or method should be considered a closed box once it has been written. If a use case comes up where the behavior needs to be adjusted, instead of changing the base class or method, it should be exteded and then this new derived class or method can adjust for the new needed behavior.
### Liskov Substitution Principle
Any object in your application should be able to be replaced with an object that is derived from it without breaking the application.
### Interface Segregation Principle
Clients should not be required to rely interfaces that they do not use. Functionality should not be joined at the hip to some massive interface, instead it should allow for smaller segments within to be used on a per need basis.
### Dependency Inversion Priciple
Code should depend on abstractions, not concrete implementations. Moreso, the details of those abstractions need to also depend on the abstractions.



[Table of Contents](README.md)