# Testing and Swagger

## Swagger
Although its not necessarily representative of its namesake's definition, it definitely has some. Swagger, more preferably known as OpenAPI, is a tool that allows humans and computers to understand the capabilities of a service without direct access it. It specifies the capabilities of your API and how to access it with HTTP. Swagger also comes with a component called SwaggerUI that creates and easily digestible view that allows for easy access and testing of the API.


## Unit Testing in ASP.NET Core
To test a controller using unit tests, the controller needs to be instantiated in the test class. A method on the controller needs to be called and a result of it stored to a variable. The result type depends on what part of the controller is being tested whether it be for a view or for returned data from an API. The specifics of the data will differ each time and may need to be compared differently, but the most common assertions will still be `Assert.Equal` or `Assert.AreEqual`.</br>
Controllers will often need input data that will be manipulated. To test its outcome, a MOQ or mocked object, is a predetermined object with set properties of which the tests will be based on. An `ActionResult` type of result of a controller action can be tested and stored in a variable in one line. Then that variable's properties can be checked on the following line(s). This same pattern can be used when testing for response types and response values.



[Table of Contents](../README.md)
