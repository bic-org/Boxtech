# API Documentation

The most beneficial way to use Boxtech is by integrating it into your workflow and systems to provide container data or a source of checking information.

The Boxtech API is part of the BIC's digital services and you will need to follow the steps below to access this API

## Steps to Access Boxtech

1. Register for an Account by visiting one of the links below:

* Live Environment: [https://app.bic-boxtech.org/sign-up](https://app.bic-boxtech.org/sign-up)
* UAT Environment: [https://uat.bic-boxtech.org/sign-up](https://app.bic-boxtech.org/sign-up)

1. Download the Postman Collection or Start Coding to Integrate

## Authentication

The value for Authorization header is: `Basic <credentials>`, where credentials is the Base64 encoding of username and password joined by a single colon `:` eg. `username:password`

Example: `Authorization: Basic QWxhZGRpbjpvcGVuIHNlc2FtZQ==`

{% swagger baseUrl="https://uat.bic-boxtech.org" path="/oauth/token" method="post" summary="Retrieve Token" %}
{% swagger-description %}

{% endswagger-description %}

{% swagger-parameter name="Authorization" type="string" required="true" in="header" %}
Base64 encoded username and password as described above.
{% endswagger-parameter %}

{% swagger-response status="200" description="" %}
```
{
    "accessToken": "eyJraWQLCJjdbWF6b25hd3MNWGwd8ixowDovA",
    "accessTokenExpiresAt": "2021-07-06T12:18:34.164521+00:00",
    "access_token": "eyJraWQiOiJPa2DovA"
}
```
{% endswagger-response %}
{% endswagger %}

## Open API Documentation and Postman Collection

Open API documentation can be found at [https://app.swaggerhub.com/apis/BIC-ORG/Boxtech/](https://app.swaggerhub.com/apis/BIC-ORG/Boxtech/)

You can download the Postman collection to get started with Boxtech at [https://documenter.getpostman.com/view/Tzm9huBX?version=latest](https://documenter.getpostman.com/view/Tzm9huBX?version=latest)
