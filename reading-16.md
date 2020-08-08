# Data Transfer Objects

## DTOs
Without implementing Data Transfer Objects (DTOs), a web API would return to the client entities directly from the database. This is usually not desireable as it could reveal extraneous or even sensitive information. There are also other potential issues such as circular references or having a payload too big to work with. DTOs act as the objects that are defined with the sole purpose of making sure that only the correct data is sent back to the client. Different DTOs can be used for the same or similar objects depending on the context of the route or what information is being requested from the API. They will inherently look very similar, but exclude data that needs to be decoupled from the service layer of the server.



[Table of Contents](README.md)