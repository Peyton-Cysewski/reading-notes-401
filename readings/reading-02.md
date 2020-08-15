# Unit Testing & Documentation

## Unit Testing Best Practices
- Meant to test specific pieces of code, one piece at a time.
- Unit testing can quickly become bulky and unwieldy, so there are frameworks that exist to help test a lot of the specific methods.
Best Practices:
- Arrange, Act, Assert: Set up a method, call it, and use the ```Assert``` class to predict the desired outcome of a success test.
- One Assert per Test Method: Self explanatory. No need to over do it.
- Avoid Test Interdependence: For testing purposes, it is wisest to test each unit independently.
- Keep it Short, Sweet, and Visible: Keep things simple and straightforward to understand.
- Recognize Test Setup Pain as a Smell: If the setup for a test is too cumbersome, then it's more likely the design needs to be simplified.
- Add Them to the Build: Don't neglect and unit tests. The worst thing that can happen is for the potential errors to build up over time due simply to laziness.

## Art of Readme
The README is the one-stop shop for anyone who wants to know anything and everything about your code base. It is where the author tells the user what the code is, how it looks in action, how to use it, and any other details pertinent to its existence. Detailed documentation can be very good, but the README needs to remain succinct. Too short or too long of a README is often a red flag.
Key Elements:
- Name: short but descriptive.
- One-liner: a short description that gives an overview for a module.
- Usage: description of a module in action.
- API: detail a module's objects, functions, signatures, return types, callbacks, and events in detail.
- Installation: self-explanatory, even if the process is common and/or straightforward.
- License: ideally put it higher up in a README so the reader can know right away if it's usage is compatible.

## ReadMe Best Practices
- Installation/Getting Started
- Features
- Configuration
- Contributing
- Helpful Links
- Licensing

These types of sections are great for a general template of a README. AS iterated above, it is best to have multiple sections that remain brief, yet cover a lot of ground in terms of introducing the application, listing features and descriptions of the code, how to install it, and anything else that is useful for the specific project.



[Table of Contents](../README.md)
