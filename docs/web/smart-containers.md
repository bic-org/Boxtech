# Smart Containers

Boxtech now supports the ability to upload Smart Container attributes to the container record, this can be done in 1 of 2 ways

1. [Upload using **fleet in** template file or API POST](smart-containers.md#upload-using-fleet-in-file)
2. [Upload only Smart Container Attributes to Boxtech](smart-containers.md#upload-smart-container-details-only)

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

### Uploading via the Web Interface

#### Upload using  'Fleet in' File

Follow the normal process for uploading your containers via the 'Fleet In' tile

<figure><img src="../.gitbook/assets/Screenshot 2023-03-22 at 13.27.43.png" alt=""><figcaption><p>Boxtech Fleet In Tile</p></figcaption></figure>

Ensure you are using the latest [Fleet In Upload Template](https://raw.githubusercontent.com/bic-org/Boxtech/master/templates/fleet-in-full.csv) which includes the smart container attributes detailed above.

#### Upload Smart Container Details Only

Once logged in to Boxtech you will see a new tile showing 'Smart Containers\`as below

<figure><img src="../.gitbook/assets/Screenshot 2023-03-22 at 13.11.40.png" alt=""><figcaption><p>Smart Containers Upload Tile</p></figcaption></figure>

Selecting this option will allow you to upload smart container attributes to your containers without uploading all technical details for the container, useful if you output this data separately or want to maintain the smart container attributes independantly.

Use the [smart container only template](https://raw.githubusercontent.com/bic-org/Boxtech/master/templates/bic\_tcd\_smart\_container\_template.csv) for the attributes and upload the file, you will receive an email on completion.

#### Viewing the Smart Container Attributes

Once you search for a container you will see for containers with smart container attributes the details as shown below

<figure><img src="../.gitbook/assets/Screenshot 2023-03-22 at 13.17.28.png" alt=""><figcaption><p>Example of Smart Container Attributes in Boxtech</p></figcaption></figure>

### Uploading via the API

For uploading using the API please see the Open API specification and documentation
