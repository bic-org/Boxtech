# INTRODUCTION

The BIC TCD Technical Characteristics Database (see [the website](http://www.bic-boxtech.org)) has as reference API which is described below. Other API entry points may be implemented on request.

* [Repository](#repository)
* [TCD API](#api)
* [Prerequisites](#prerequisites)
* [Detailed samples](#samples)
* [Manual Tests with a REST Client](#manualtests)


## Repository <a id="repository"></a>

This repository contains samples for calling the TCD REST API. These API samples are open source. Other samples may be contributed by you or others to the GitHub repository : please fork and suggest your pull requests.


## TCD API <a id="api"></a>

The TCD API is a simple REST API.

The following entry points are available, for looking up tare information in the TCD :
- **tare_kg**  : for a given container number, provides the tare in kg
- **tare_lbs** : for a given container number, provides the tare in lbs

The following entry points are planned, but not yet available, for updating the TCD :
- **fleet_in** : declare a new container in my fleet
- **fleet_out** : declare that a container has left my fleet
- **fleet_replace** : upload a file with the whole contents of my fleet, replacing the existing contents


## Prerequisites <a id="prerequisites"></a>

To use the TCD API, you will need the following :

### **Username** and **Password**
You will be given these once you have signed up on the TCD app : see [BIC TCD website](http://www.bic-boxtech.org)
Remember that, from time to time, you may need to approve new Terms and Conditions : to do this, simply log in manually into the app : see [the FAQ](http://www.bic-boxtech.org/faqs)

### **Clientid**

You will use the following value for **clientid** in your tests and in your app :
- for production and sandbox, **clientid** is YmljYXBwOmJpY3NlY3JldGFwcA==

### Endpoint

The endpoint for the TCD REST API is :
- for Production : app.bic-boxtech.org/api
- for Sandbox : test-bic-container.herokuapp.com/api

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
