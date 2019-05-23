# Error Handling

## Error Response Structure

All 400 errors encountered during request will render the same error structure.

> 400 Error Response Structure

```json-doc

{
    "error": {
        "name": "Error",
        "status": 400,
        "message": "Request data validation error",
        "errors": [
            {
                "failed": "required", // The condition that failed
                "path": [
                    "hotelName" // parameter that caused an error
                ]
            }
        ]
    }
}

```

The API uses the following error codes:

Error Code | Meaning
---------- | -------
400 | Bad Request -- 	The request cannot be fulfilled due to bad syntax.
401 | Unauthorized -- The end-point requested is not allowed.
403 | Forbidden -- The end-point requested is not allowed.
404 | Not Found -- The end-point requested could not be found.
405 | Method Not Allowed -- You tried to access an end-point with an invalid method.
406 | Not Acceptable -- You requested a format that isn't json.
410 | Gone -- The request end-point requested has been removed from our servers.
429 | Too Many Requests -- You're making too many requests! Slow down!
500 | Internal Server Error -- We had a problem with our server. Try again later.
503 | Service Unavailable -- We're temporarily offline for maintenance. Please try again later.
