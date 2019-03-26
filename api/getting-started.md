First of all you need to [create an application](creating-an-application.md).

After registering the app you will receive credentials for [authentication](authentication.md).

Base API URL is https://digital-quran.quranacademy.org.

## General concepts

- API works exclusively over HTTPS
- API always returns HTTP code 200 if the request handled was correctly handled by the server
- API returns data in JSON format
- Every API request must include "Language" header with the code of a language. See the [list of available languages](available-languages.md).
- Every request to the API must be authenticated
