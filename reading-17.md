# Intro to Identity

## Adding Identity in ASP.NET Core
When setting up an ASP.NET Core application that will use identities, in the `startup.cs` file in the `ConfigureServices` method, all of the associated identity properties for the application need to be added. In the `Configure` method, `app.UseAuthentication` needs to be added to make sure the proper middleware is used. 

## Behind the Scenes of Identity
There are five verbs associated with identities and authentication:</br>
- Authenticate: Getting the user's information (assuming it exists).
- Challenge: Requests authentication by the user.
- SignIn: Persists the user's information somewhere.
- SignOut: Removes the user's persisted information.
- Forbid: Denies access to a resource for unauthenticated users or authenticated but unauthorized users.</br>
Authentication handlers in ASP.NET Core are handled by the Cookies authentication handler. The authentication middleware is inserted upon startup in the startup file. The authentication handler will authenticate the user and pass it on to the authentication middleware that creates the `HttpContext.User` object with the returned information.



[Table of Contents](README.md)