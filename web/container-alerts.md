# Container Alerts

## Alert Types

Boxtech contains a series of alerts grouped as:

* Sold 
* Scrapped
* Lost
* Stolen 

If an alert is active for a container it will be shown on the search results and in the API response for that container.

In all cases Boxtech will continue to show the container details for the container, but in all cases the alert type and text will be provided when active.

### Sold 

The container has been sold by the BIC Code Holder and is no longer part of their owned fleet, containers that have been sold should be remarked by the new owner if they are to continue circulation for International movements.  

Boxtech will continue to show the container details for the container, but in all cases the alert type and text will be provided.

{% hint style="info" %}
It is possible to make a declaration of sale for containers where you are not the BIC Code Holder for the container.  The process is the same as Sold, the container will be shown with an alert to indicate you have made a 'public record of sale', this date of this alert will also be timestamped by Boxtech and viewable by anyone searching for the container.
{% endhint %}

### Scrapped 

The container has been scrapped by the BIC Code Holder and is no longer part of their owned fleet, containers that have been scrapped would not normally continue circulation for International movements, the intention is that the container has been or is being disposed of.

Boxtech will continue to show the container details for the container, but in all cases the alert type and text will be provided.

### Lost

The container is flagged as lost by the BIC Code Holder, meaning that whilst it is still in their fleet the whereabouts of the container are currently unknown, anyone finding this container should contact the BIC Code Holder.

### Stolen

The container is flagged as stolen by the BIC Code Holder, meaning that whilst it is still in their fleet the whereabouts of the container are currently unknown, the theft of the container has been reported to authorities and a police report filed.  Anyone finding this container should contact the BIC Code Holder and local Police.

## Activating or Deactivating Alerts in Boxtech

To activate or deactivate alerts you must have `uploader` rights in Boxtech.

Once logged in you have 2 options:

* Sold/Scrapped 
* Lost/Stolen

Select the category of alert, and follow the onscreen instructions if uploading your alert template in csv format.  You will specify in the upload if you wish to activate or deactivate the alert.

You can also integrate Boxtech into your application and activate or deactivate your alerts using the API endpoints documented in the [Open API Specification ](../api/api-documentation.md)

![Uploader Screen](../.gitbook/assets/image%20%282%29.png)

