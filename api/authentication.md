# Authentication

Every app has an application access token, client ID and client secret.

All endpoints of the API are separated to public and user specific.

**Public endpoints** require only an application access token. For example, getting list of surahs does not require a user to log in.

**User specific endpoints** require authentication from a specific user.

## Public endpoints authentication

To authenticate requests to public endpoints you need to send the application access token in `Access-Token` HTTP header.

The access token identifies your app, it is not bound to an IP address and its validity period is not limited. If the access token has been compromised, you can generate a new token, and the old one will be canceled.

Example of application access token:

```text
T0IfpQun1HpkgNo7LHQP1fjN6cHOo6mReu2Qlts7XZCO5MqhDxTZ8beaXNBQNkCz
```

## User specific endpoints authentication

This feature is not implemented yet.

Client ID and client secret are used for user authentication.

The client ID is considered public information and is used to build login URLs or included in source code. The client secret must be kept confidential.

Example of client ID and client secret:

```text
CLIENT_ID: BdWshXtYr8P6bVkAD8yuMkfeBGIkLmwlz1vJMYFkxpJ8WtURmfkwH9PvdjjukQGL
CLIENT_SECRET: DF1n0DFdq02xjnBZDpEpfJOZ8joMF1dKHGTnX1bRoBph0XPN4zPO1VX0ZLpAvgAX
```

