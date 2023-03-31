# Automating the Updates

Now you have uploaded your container fleet to Boxtech you will need to think about keeping it updated, there are a few ways to do this and the key part is to establish a process that fits well with your system and internal process, Boxtech has a number of options:

1. **Upload** on a regular basis through the website [https://bic-boxtech.org](https://bic-boxtech.org)&#x20;
2. Send the file to Boxtech using **SFTP** on a schedule
3. Integrate the **API** into your system and container process

We would recommend that you consider automating your updates to Boxtech, this ensures your fleet is regularly updated in Boxtech and makes the uploading process more efficient. &#x20;

If you output reports to update Boxtech then **option 2** maybe a good way to automate the updates, using SFTP is like having a shared folder between your organisation and Boxtech, your system securely connects to the shared folder on Boxtech and uploads the same format report that you would use if logging into the website.  This approach can be for as little as 1 container or up to a fleet file of millions of containers.  This approach is recommended if you want to provide periodic updates and can produce outputs in CSV format from your system, it's straightforward for your IT team to implement. &#x20;

If your system is event driven and you want to add hooks into those events to update Boxtech on a container by container basis then the API is a good option, usually you would perform a fleet upload, and then send messages as changes take place in your system for each container, in simple language terms

> When new container added to the fleet send a NEW CONTAINER message with technical details to Boxtech
>
> For each container sold in my system send a SOLD alert to Boxtech

This approach will mean implementing the Boxtech API into event messages from your system, enabling it to send messages to Boxtech when a system 'event' happens.  A great way to be fully integrated with Boxtech, it requires a little more in terms of IT resource and planning, your IT department will want to look at the API Specification and it's useful to setup a call with the BIC team to familiarise you with the API and give you test platform access.

### Requesting SFTP or API Access

To request access and setup for SFTP or API please contact the BIC team by email at [info@bic-boxtech.org](mailto:BIC%20BoxTech%20%3Cinfo%40bic-boxtech.org%3E) noting your BIC Code and that you would like to upload by API or SFTP.

