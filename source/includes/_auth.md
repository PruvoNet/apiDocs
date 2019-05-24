# Authorization

This section describes the authorization process.

Every request to any available endpoint requires authorization. To get the authorization credentials you need an active partner account registered within Pruvo’s systems.

The following table details the required headers that must be sent with each request.

Header key | Header value | Description 
---------- | ------- | ------- 
`Authorization` | Authorization Key | Key provided by Pruvo 
`API-Version` | Api Version | PI Version to use 

If you prefer not to send the authorization data as headers, you can send them as query parameters:

Key | Value | Description 
---------- | ------- | ------- | ------- 
`access_token` | Authorization Key | Key provided by Pruvo 
`api_version` | Api Version | PI Version to use 

