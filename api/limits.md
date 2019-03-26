# Limits

Requests are rate limited to 600 requests per minute.

When you make a request to the API you'll receive `X-RateLimit-Limit` and `X-RateLimit-Remaining` headers in the response.

If you exceed the number of valid requests, you will receive the error "TOO_MANY_REQUESTS".
Its rate limit will be reset after a minute interval.
Your implementation should expect and be able to handle this by waiting a minute before making additional requests.

If the rate limit is too low for your application, please contact our support team ([digitalquran@quranacademy.org](mailto:digitalquran@quranacademy.org)).

