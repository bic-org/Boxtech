# Limits and Quotas

This section describes the limits and quotas of the BIC Boxtech API.

Boxtech: Global Container Database provides supply chain safety and efficiency through data visibility: a non-profit platform for container technical details. &#x20;

To enable us to provide the service as a non profit and service the volume of requests we have put limits and quotas on API requests.  The limits and quotas are subject to change.

### Quota Limits

The following apply to 'consumers' of the API, for a container fleet 'uploader' these do not apply.  Each API query to Boxtech is for a single container only, and counts as a 'query', it is not possible to query for multiple units at a time.

* 5,000 queries per month&#x20;
* 300 for containers marked with the same [BIC Code](https://www.bic-code.org/bic-codes/) per day
* 30 queries per second&#x20;

{% hint style="info" %}
If your usage is exceeding the above limits then please contact BIC to explain your use case for Boxtech in which case it will be evaluated and you may be granted a higher tiered usage plan.  Acceptable requests for higher usage are generally reserved for container depot operators, terminals, carriers, and feeder operators.  BIC fully support the use of Boxtech for larger users so please [contact BIC](https://www.bic-boxtech.org/contact/) for a higher usage plan.
{% endhint %}

### Exceeding Quota Limits

If the quota is exceeded, the API will return an error code `429 (Exceeded Quota)` or `423 (Suspended Account)` and a message that the account has exceeded the quota or been suspended, see the [terms and conditions](https://www.bic-code.org/api-terms-of-use/) for more information.
