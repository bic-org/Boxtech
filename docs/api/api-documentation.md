# API Documentation

The most beneficial way to use Boxtech is by integrating it into your workflow and systems to provide container data or a source of checking information.

The Boxtech API is part of the BIC's digital services and you will need to follow the steps below to access this API

## Steps to Access

1. Register for an Account at [https://app.bic-boxtech.org/sign-up](https://app.bic-boxtech.org/sign-up)
2. Download the Postman Collection or Start Coding to Integrate

## Authentication

The value for Authorization header is: `Basic <credentials>`, where credentials is the Base64 encoding of username and password joined by a single colon `:` eg. `username:password`

Example: `Authorization: Basic QWxhZGRpbjpvcGVuIHNlc2FtZQ==`

{% api-method method="post" host="https://boxtech.cif-consulting.co.uk" path="/oauth/token" %}
{% api-method-summary %}
Retrieve Token
{% endapi-method-summary %}

{% api-method-description %}

{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-headers %}
{% api-method-parameter name="Authorization" type="string" required=true %}
Base64 encoded username and password as described above.
{% endapi-method-parameter %}
{% endapi-method-headers %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
Once valid credentials are supplied, a valid access token is returned.
{% endapi-method-response-example-description %}

```text
{
    "accessToken": "eyJraWQLCJjdbWF6b25hd3MNWGwd8ixowDovA",
    "accessTokenExpiresAt": "2021-07-06T12:18:34.164521+00:00",
    "access_token": "eyJraWQiOiJPa2DovA"
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

## Open API Documentation and Postman Collection

Open API documentation can be found at...

You can download the Postman collection to get started with Boxtech at [https://documenter.getpostman.com/view/Tzm9huBX?version=latest](https://documenter.getpostman.com/view/Tzm9huBX?version=latest)

