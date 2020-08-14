# Policies

## What are Policies?
Polices are essentially checkpoints that only let the user through if they meet certain requirements. This is applied specifically to routes and common is checking for either a role or a claim to authorize the user to proceed. Authorization is added in the `ConfigureServices` method in the startup file. Within this, policies can be added with specific requirements.</br>
The service responsible for handling authorization is the `IAuthorize` interface. Within this,`IAuthorizationRequirement` and `IAuthorizationHandler` handle the dirty work. To use these policies on routes use the attribute `[Authorize(Policy = "<policy name here>")]` to make it require a specific policy that has been listed in the startup file.

## Custom Policies
It is possible to make customizable policies using `IAuthorizationPolicyProvider`. This allows for a wide range of policies to be added instead of many individual `AuthorizationOptions.AddPolicy` calls. Within that interface `GetPolicyAsync`, `Get DefaultPolicyAsync`, and `GetFallbackPolicyAsync` are the APIs that allow for full customization.



[Table of Contents](README.md)