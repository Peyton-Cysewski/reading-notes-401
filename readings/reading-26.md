# OAuth

## The OAuth Flow
The first step in any OAuth cycle is to register an application with whatever service provider you are looking to work with. For example, Spotify has a backend API but to use it you have to register an application with them. Once this is done, the service provider will supply you with a Client ID and a Client Secret. Once the is complete, the OAuth flow goes as follows:</br>
- The Consumer makes a request to the Service Provider authorization endpoint to authorize the user.
- The Service Provider authenticates the user and prompts them whether to authorize the Consumer to access their information.
- If the user authorizes the Consumer, the Service Provider redirects back to the redirect URI on the Consumer’s website with a temporary access code.
- The Consumer calls the token endpoint on the Service Provider website to exchange the code for a more permanent access token.
- The Service Provider grants an access token which can be used to authenticate subsequent requests to protected resources</br>
The endpoints mentioned above like the authorization endpoint or token endpoint should be provided in the service provider's documentation. The important part is the information you provide whether it be the ID or the Secret.

## Using OAuth in ASP.Net Core
In the Startup class you need to register the proper middleware: `AddAuthenitcation()`, `AddCookie()`, and `AddOAuth()`. Each portion has many subcategories that need to be assigned, but these are the baseline statup registration requirements. Once all of these are set up there needs to be a way to challenge the authentication handler. In the controller for the login functionality, it needs to return a `Challenge` and an `IActionResult`. From here, it is all a matter of grabbing the information sent in JSON form to dispaly or use in views. These can be grabbed by using `options.ClaimActions.MapJsonKey({specifics here}, {and here})` in the `AddOAuth()` middleware. This will map the properties directly into key, value pairs on the user's claim. That is where they will be accessible for use.



[Table of Contents](../README.md)