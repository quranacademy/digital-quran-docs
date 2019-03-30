# Errors

- If the server returned status code not equals 200 then an error occured.
- You should always check that the response is a valid JSON.

If an error occurs during the request, the server will return the response in the following format:

```json
{
    "error": {
        "code": "ERROR_CODE",
        "message": "Message with error description."
    }
}
```

The response status code will be 200, not 4xx or 5xx, because it's not a REST API. If the server returned a response with code 4xx or 5xx it means that something went wrong and the server couldn't handle a error correctly, so the response may be an  invalid JSON.

You have to handle the both cases: if the response status code is not equals 200 and if the response contains the field "error".

Every endpoint may have it's own error codes but there are also common error codes.

## Common error codes

**UNKNOWN_ERROR**

Unknown error occurred. Typically a server bug.

**NOT_FOUND**

Endpoint not found. Check request URL is correct.

**TOO_MANY_REQUESTS**

Too many requests.

**ACCESS_TOKEN_NOT_PROVIDED**

Access token is not provided.

**INVALID_ACCESS_TOKEN**

Access token is invalid.

**LANGUAGE_NOT_PROVIDED**

"Language" header is not provided.

**INVALID_LANGUAGE**

Invalid language code provided. See the [list of available languages](available-languages.md).

**INVALID_PARAMETERS**

Invalid parameter(s) provided.

This error means that some of passed parameters are invalid. In response you will get `validation_errors` field with validation error messages.

Example:

```json
{
    "error": {
        "code": "INVALID_PARAMETERS",
        "message": "Some of passed parameters are invalid"
    },
    "validation_errors": {
        "surah": "Surah number must be an integer from 1 to 114"
    },
}
```

**INTERNAL_SERVER_ERROR**

Internal server error occurred. Typically a server bug.