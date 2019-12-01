# Getting started

{% hint style="warning" %}
API is currently under development. Stay tuned to the [project repository](https://github.com/quranacademy/digital-quran-docs) on GitHub.
{% endhint %}

First of all, you need to [create an application](creating-an-application.md).

After registering the app you will receive credentials for [authentication](authentication.md).

Base API URL is [https://digital-quran.quranacademy.org](https://digital-quran.quranacademy.org).

## General concepts

* API works exclusively over HTTPS.
* Every API request must be performed using POST method.
* Every API request must be a valid JSON and include "Content-Type: application/json" header.
* Every API request must include the "Language" header with the code of a language. See the [list of available languages](https://github.com/quranacademy/digital-quran-docs/tree/897278b43c9c88853ed2c939278b8d7f042acb77/api/available-languages.md).
* Every request to the API must be authenticated.
* API always returns HTTP code 200 if the request handled was correctly handled by the server.
* API returns data in JSON format.

