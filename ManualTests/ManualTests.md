---
layout: default
title: Get Started
nav_order: 2
---

# Using an API Client

The easiest way to test the BoxTech API is to use a REST Client such as Postman see [http://www.getpostman.com](http://www.getpostman.com/downloads/)) which can be run in your browser or on your desktop.  This client access will help you understand the API before starting to write code to automate the calls.

**This guide will take around 10 minutes to complete**

## Signup for Boxtech API

Visit [https://www.bic-boxtech.org/sign-up/](https://www.bic-boxtech.org/sign-up/)
* Signup for a new user account to access data.  Accept Terms and Conditions.
* Confirm your account activation by clicking the link received by email.

You now have a <username\> and <password\> you can use in the API.

## Get hold of Postman

Download Postman to your desktop or run it in your browser.
Create a (free account) to save your tests for future reference.

## Authentication

Now you are in postman, create a 'New Tab' at the top of the screen

![New tab in Postman](./images/01_New_Tab.png)

Configure the BoxTech API Authentication call :
- select the POST operation
- enter `https://app.bic-boxtech.org/oauth/token` for the URL
- add 2 headers in the Headers section

| **Key** | **Value** |
| ------- | --------- |
| Content-Type | application/x-www-form-urlencoded |
| Authorization | Basic YmljYXBwOmJpY3NlY3JldGFwcA== |

*Note : the value of the Authorization key is called the <clientid\>*

![Authentication headers](./images/02_Auth_Headers.png)

Move to the Body section :
- select the x-www-url-encoded type of body
- add 3 values in the body

| **Key** | **Value** |
| ------- | --------- |
| grant_type | password |
| username | *your_username* |
| password | *your_password* |

- save your work by clicking Save on the right, and store it in a collection you will call BIC BoxTech

![Authentication body](./images/03_Auth_Body.png)

Click Send : you should get a response which looks like this :

![Authentication body](./images/04_Auth_Response.png)

Grab the `access_token` value, in our case : `0b59efa0ddf2b2764eb0501be6c312d0e8dc92eb`

## Call GET container API

In Postman, create a new tab at the top of the screen.

Configure the BoxTech API get container call :
- select the GET operation
- use the `https://app.bic-boxtech.org/api/v2.0/container/GLDU5334260` URL : this will query for the GLDU5334260 container. Note the format of the container number which includes the check digit
- add 1 header in the Headers section

| **Key** | **Value** |
| ------- | --------- |
| Authorization | Bearer *access_token* |

*NOTE: Replace the `access_token` with the one you retrieved previously, in our example `0b59efa0ddf2b2764eb0501be6c312d0e8dc92eb`*


- save your work which should look like this :

![Get headers](./images/05_Get_Headers.png)

Click Send : you should get a response like this :

![Tare_kg response](./images/06_get_Response.png)

The `tare_kg` of the container is 2230 kg.
