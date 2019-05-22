# Authorization

This section describes the authorization process.

Every request to any available endpoint requires authorization. To get the authorization credentials you need an active partner account registered within Pruvo’s systems.

The following table details the required headers that must be sent with each request.

Header key | Header value | Description | Example
---------- | ------- | ------- | ------- 
`Authorization` | Authorization Key | Key provided by Pruvo | `bf93c4e2-36d6-413c-aa86-46c1b108215d`
`API-Version` | Api Version | PI Version to use | `1.0` 

If you prefer not to send the authorization data as headers, you can send them as query paramters:

Key | Value | Description | Example
---------- | ------- | ------- | ------- 
`access_token` | Authorization Key | Key provided by Pruvo | `bf93c4e2-36d6-413c-aa86-46c1b108215d`
`api_version` | Api Version | PI Version to use | `1.0` 

