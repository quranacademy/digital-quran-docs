# Limits

Requests are rate limited to 600 requests per minute.

When you make a request to the API you will receive the following headers in the response:

* **Rate-Limit**: What’s the rate limit available to you. The default is 600.
* **Rate-Limit-Remaining**: How many requests are available to you. This will be 600 minus all the requests you have done.
* **Rate-Limit-Over**: How many requests over your quota you have made.
* **Rate-Limit-Reset**: The UTC date and time of when your quota will be reset.

You can see how much of your quota has been used by checking this headers.

Example:

```text
Rate-Limit: 600
Rate-Limit-Remaining: 354
Rate-Limit-Over: 0
Rate-Limit-Reset: 1453180594367
```

If you exceed the number of valid requests, you will receive the error "TOO\_MANY\_REQUESTS". Its rate limit will be reset after a minute interval. Your implementation should expect and be able to handle this by waiting a minute before making additional requests.

```javascript
{
    "error": {
        "code": "TOO_MANY_REQUESTS",
        "message": "Too many requests."
    }
}
```

If the rate limit is too low for your application, please contact our support team \([digitalquran@quranacademy.org](mailto:digitalquran@quranacademy.org)\).

