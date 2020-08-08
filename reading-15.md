# Claims and JWT Tokens

## Authentication vs Authorization
Authentication is simply the process of determining who you are while Authorization is the process of determining what you are allowed to do.

## Claim-based Authorization
- Claim: a value pair that represents what an identity is, not what it can do.
Claim based authorizaton essentially is done by checking the claim and its value. Depending on what the value is, the identity would have access to certain resources. The claim also has an issuer and the checker would have to trust it to validate the claim. If the claim issuer isn't trusted, then it doesn't matter what claim says at all. In ASP.NET Core policies are added in the startup file that can check the claim and then be added to routes making them require a passing claim to access that route and its resources. Policies can also be attached to the full controller which makes it apply to all connected routes.</br>
There is a property `User` in `HttpContext` that allows for the claim to be directly referenced. Now it is more proper to use `ClaimsPrincipal` as a claims-based way of authorization as opposed to a role-based authorization.

## JWT Authentication
- JWT: JSON Web Token. These are used to pass claims between parties. It is signed with a JSON Web Signature and encoded using JSON Web Encryption.
A JWT is broken into three parts, the Header, the Payload, and the Signature:
- Header: Contains the algorithm that will be used to verify the token and the type of token, obviously a JWT. Encoded with `encodeBase64Url`.
- Payload: This can be all the custom data that is meant to be passed along, as well as the claims associated with the identity. Encoded with `encodeBase64Url`.
- Signature: This part is comprised of a secret key hashed together with the result of the concatenated `encodeBase64Url` of the header and payload with a period in between them. This hash is unique and is only verifiable with the secret key. 



[Table of Contents](README.md)