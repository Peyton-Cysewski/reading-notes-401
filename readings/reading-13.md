# Basic Routing

## Routing within MVC
Web routing is enabled in two places: `Web.config` and `Global.asax.cs`. The second file is of greater importance because it contains event handlers for the application. Each route that is handled has three parts: the controller, the action, and an optional ID. There is always a default route with all three being `Home/Index/?Id`. In this case (assuming Id is 3 for example), the code that would be executed is `HomeController.Index(3)`.

## Routing within Core
- `UseRouting` - Adds route matching to the middleware pipeline. This middleware looks at the set of endpoints defined in the app, and selects the best match based on the request.
- `UseEndpoints` - Adds endpoint execution to the middleware pipeline. It runs the delegate associated with the selected endpoint.
Note: There are many other parts of the middleware that can be used in conjunction with these methods such as for authorization, but these are the primary ones.



[Table of Contents](../README.md)
