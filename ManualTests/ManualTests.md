---
layout: default
title: Get Started
nav_order: 2
---

# Using an API Client

The easiest way to test the BoxTech API is to use a REST Client such as Postman see [http://www.getpostman.com](http://www.getpostman.com)) which can be run in your browser or on your desktop.  This client access will help you understand the API before starting to write code to automate the calls.

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
- enter http://app.bic-boxtech.org/oauth/token for the URL
- add 2 headers in the Headers section :

| **Key** | **Value** |
| Content-Type | application/x-www-form-urlencoded |
| Authorization | Basic YmljYXBwOmJpY3NlY3JldGFwcA== |

*Note : the value of the Authorization key is called the <clientid\>*

![AUthentication headers](./images/02_Auth_Headers.png)

Move to the Body section :
- select the x-www-url-encoded type of body
- add 3 values in the body :
+ key = grant_type, value = password
+ key = username, value = <your_username\>
+ key = paswsword, value = <your_password\>
- save your work by clicking Save on the right, and store it in a collection you will call BIC BoxTech
![Authentication body](./images/03_Auth_Body.png)

Click Send : you should get a response which looks like this :
![Authentication body](./images/04_Auth_Response.png)

Grab the "accessToken" value, in our case : 784b64f338a812343915c6f4734d2f71fe14a68d

## Call Tare_kg

In Postman, create a new tab at the top of the screen.

Configure the BoxTech API Tare_kg call :
- select the GET operation
- use the http://test-bic-container.herokuapp.com/api/tare_kg/GLDU5334260 URL : this will query for the GLDU5334260 container. Note the format of the container number which includes the check digit
- add 1 header in the Headers section :
+ key = Authorization, value = Bearer 784b64f338a812343915c6f4734d2f71fe14a68d (or in your case, Bearer followed by the <accessToken\> you saved previously, separated by a blank space)
- save your work which should look like this :
![Tare_kg headers](./images/05_Tare_kg_Headers.png)

Click Send : you should get a response like this :
![Tare_kg response](./images/06_Tare_kg_Response.png)

The tare weight of the container is 2232 kg.

## Call Tare_lbs

You can practise on your own creating a new test in a new tab to call the tare_lbs service, with the same parameters, to query for the tare weight in lbs.

## Same tests in Production

To run the same tests in the BIC BoxTech Production database :
- signup for a "Data access only" user in production. Accept Terms and Conditions. Confirm your account activation by clicking the link received by email. You now have a production <username\> and <password\> you can use in the API in production
- use the http://app.bic-boxtech.org/oauth/token URL for authentication in production
- use the http://app.bic-boxtech.org/api/tare_kg URL for the Tare (kg) service in production
- use the http://app.bic-boxtech.org/api/tare_lbs URL for the Tare (lbs) service in production
