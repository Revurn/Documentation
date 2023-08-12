# Errors

The Revurn API has the following error codes.


Error Code | Meaning
---------- | -------
400 | Bad Request -- Your request is invalid.
401 | Unauthorized -- Your Token is invalid.
403 | Forbidden -- You cannot access this resource.
404 | Not Found -- The endpoint you requested could not be found
405 | Method Not Allowed -- The requested API method is not allowed
406 | Not Acceptable -- You requested a format that isn't json.
418 | I'm a teapot.
429 | Too Many Requests -- You are sending too many requests to the Revurn API
500 | Internal Server Error -- We had a problem with our server. Try again later.
503 | Service Unavailable -- We're temporarily offline for maintenance. Please try again later.
