# Errors

- If the server returned status code not equals 200 then an error occured.
- You should always check that the response is a valid JSON.

If an error occurs during the request, the server will return the response in the following format:

```json
{
    "error": "ERROR_CODE",
    "error_message": "Message with error description"
}
```

The response code will be 200, not 4xx or 5xx, because it's not a REST API.

If the server returned a response with code 4xx or 5xx it may be not a valid JSON.

Each endpoint may have it's own error codes but there are also common error codes.

Common error codes:

- UNKNOWN_ERROR - Unknown error occurred.
- NOT_FOUND - Endpoint not found.
- TOO_MANY_REQUESTS - Too many requests.
- ACCESS_TOKEN_NOT_PROVIDED - Auth token is not provided.
- INVALID_ACCESS_TOKEN - Auth token is invalid.
- LANGUAGE_NOT_PROVIDED - Language code is not provided.
- INVALID_LANGUAGE - Invalid language code provided.
- INVALID_PARAMETERS - Invalid parameters provided.
- INTERNAL_SERVER_ERROR - Internal server error occured.

## Troubleshooting

**UNKNOWN_ERROR**

Typically a server bug.

**NOT_FOUND**

Check request URL is correct.

**INVALID_ACCESS_TOKEN**

Check your access token is valid.

**INVALID_LANGUAGE**

Check specified language is available. See the list of available languages.

**INVALID_PARAMETERS**

This error means that some of passed parameters are invalid. In response you will get `validation_errors` field with validation error messages.

For example:

```json
{
    "error": "INVALID_PARAMETERS",
    "error_message": "Some of passed parameters are invalid",
    "validation_errors": {
        "surah": "Surah number must be an integer from 1 to 114"
    },
}
```

**INTERNAL_SERVER_ERROR**

Typically a server bug.
