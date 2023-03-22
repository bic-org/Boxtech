# Smart Containers

Boxtech now supports the ability to upload Smart Container attributes to the container record, this can be done in 1 of 2 ways

1. Include in your fleet in template file or API POST
2. Upload only Smart Container Attributes to Boxtech

The purpose of the smart container details to is assist with the safety aspects of containers and planning at terminals.



### Smart Container Attributes&#x20;

Smart Containers have the following Attributes which can be added

| Boxtech Field                   | Allowable Values      | Description                                                                                                                                                                 |
| ------------------------------- | --------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| container\_number               | BICU1234567           | Container number of which to apply the smart container data fields                                                                                                          |
| smart\_container                | `YES` or `NO`         | Indicate if the container is equiped with a smart device                                                                                                                    |
| smart\_container\_certification | `UNKNOWN`, `A1`, `A2` | Which certification is applied to the smart container device, for meanings [see here ](https://github.com/bic-org/referencedata/blob/main/smartcontainercertifications.csv) |
| smart\_container\_activated     | `YES` or `NO`         | Indicate if the device is active or deactivated                                                                                                                             |



If you are uploading only the smart container attributes you can use the specific template [available here](https://raw.githubusercontent.com/bic-org/Boxtech/master/templates/bic\_tcd\_smart\_container\_template.csv) this can be used by either the BIC Code Holder or an IOT provider, the option of uplaod via an API POST is also available.
