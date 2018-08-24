# INTRODUCTION

The BIC BoxTech Containers Database (see [the website](http://www.bic-boxtech.org)) has a reference API which is described below. Other API entry points may be implemented on request.

* [Repository](#repository)
* [BoxTech API](#api)
* [Prerequisites](#prerequisites)
* [Detailed samples](#samples)
* [Manual Tests with a REST Client](#manualtests)


## Repository <a id="repository"></a>

This repository contains samples for calling the BoxTech REST API. These API samples are open source. Other samples may be contributed by you or others to the GitHub repository : please fork and suggest your pull requests.


## BoxTech API <a id="api"></a>

The BoxTech API is a simple REST API.

you can find its specification [over here.](https://bic-boxtech.github.io/BIC-Boxtech-API-documentation/index.html)




## Prerequisites <a id="prerequisites"></a>

To use the BoxTech API, you will need the following :

### **Username** and **Password**
You will be given these once you have signed up on the BoxTech app : see [BIC BoxTech website](http://www.bic-boxtech.org)
Remember that, from time to time, you may need to approve new Terms and Conditions : to do this, simply log in manually into the app : see [the FAQ](http://www.bic-boxtech.org/faqs)

### **Clientid**

You will use the following value for **clientid** in your tests and in your app :
- for production and sandbox, **clientid** is YmljYXBwOmJpY3NlY3JldGFwcA==

### Endpoint

The endpoint for the BoxTech REST API is :
- for Production : https://app.bic-boxtech.org/api/v2.0
- for Sandbox : https://test-bic-container.herokuapp.com/api/v2.0

### Container number

For Sandbox, you may test you tare request with the following container number : GLDU5334260
Generally speaking, the container number format is AAAU9999999 :
- BIC Code of 4 characters
- Container number with 6 digits plus 1 check digit.


## Detailed Samples <a id="samples"></a>

A simple flow would be the following :
- call the authentication service with username/password; this returns a token used in all other API calls
- call the tare_kg entry point, passing the authentication token and the container number; this returns the tare in kgs 

The following chapters describe how to use the API :

1. [AUTHENTICATION](../../wiki/Authentication)

2. [TARE_KG, TARE_LBS](../../wiki/Tare-Weight) : how to call these entry points

3. [ERRORS](../../wiki/Errors) : details about error codes and messages


## Manual Tests with a REST Client <a id="manualtests"></a>

We have added a step-by-step description of manual tests we suggest you run with Postman, a REST Client application :
- sign up for a sandbox user for data access only
- authenticate with this user to get a token
- call the tare_kg service with this token to look up the tare weight of a container
- repeat the operation in production

More details [in this guide](./ManualTests/ManualTests.mdown)


## Feedback and Support

We invite you to add your comments about the Tare Weight API service here as comments on this GitHub issue :
	https://github.com/bic-boxtech/BIC-BoxTech-API-Samples/issues/1
	
If you have other problems or questions, we invite you to enter them here as a new issue :
	https://github.com/bic-boxtech/BIC-BoxTech-API-Samples/issues/new

** Please do not look for support by email - response time on GitHub will be much faster **
