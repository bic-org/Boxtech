# Managing your Fleet

## Steps

1. Request `Uploader Access` for your BIC Code
2. Await Verification by BIC
3. Start Managing your Fleet

## Uploader Access Request

You can request access as an uploader on the registration form when first registering for access to Boxtech, it is also possible to request access once logged in if it is required at a later time.

You will just need to provide a BIC Code Prefix which will be used to verify your relationship to the BIC Code Holder's account in Boxtech, this is checked with the contact that registered the BIC Code from your organisation, they will receive an email from the BIC which they can confirm your request by clicking the button within the email.

## BIC Code Holder and Current Operator

There are two parties that are often required to be known for a container, and these are the definitions and how they are determined:

### BIC Code Holder

The owner of the BIC Prefix that is marked on the container, this company hold an account with BIC and are the registered code holder.  This could be for example a lessor, carrier or shipper with own containers.

### Current Operator

If the container is marked with a BIC prefix belonging to a lessor, they may not be the current operator of the container, as it will likely be 'on hire' to another company.  When an `uploader` provides their fleet to Boxtech, if they are not the BIC Code Holder they will become the current operator, when they off hire OR another company on hires and uploads their fleet they will be removed and the new operator added.

## Action Types 

Boxtech contains a 2 types of action when it comes to managing your container fleet:

* Fleet In / On Hire
* Fleet Out / Off Hire

You may have containers within your fleet that you own or lease, you can manage them through these actions.

### Fleet In / On Hire

The containers being uploaded are currently in your active fleet of containers, meaning you either own the containers or they are 'on hire' to you from a lessor.

If you own the BIC Code Prefix you will be noted as the **BIC Code Holder** for these containers, as well as the **Current Operator**.  You will also be able to update the container details as the official owner.

If you are leasing these containers and do not own the BIC prefix you will be identified as the **Current Operator** only, the **BIC Code Holder** will be automatically identified.

### Fleet Out / Off Hire

The containers being uploaded are to be removed from your active fleet of containers.  You can perform this action when the container is either owned by you and you are identified as the **BIC Code Holder** OR you are the **Current Operator** of the container.

If the container is on hire to you, performing this action will remove you from the Current Operator field, meaning the container is no longer operated within your fleet.

If you also own the BIC Code Prefix you will be noted as the **BIC Code Holder** for these containers, in this case the off hire process is used to manage the **lease back container** use case in which the containers are owned by a leasing company but marked with your BIC Code Prefix.  In this case you would be removed as the current operator of the container \(as it is no longer in operation of your fleet\) and an alert would be raised against the container showing that the container was a leaseback and is no longer under your fleet and thre container number is no longer valid.

## Use Cases

Some typical examples of use cases and when to interact with the Fleet In / Out funcationality.

### New Containers added to Fleet

In this case you would simply add the containers to the template and upload using the **fleet in** feature.  This will add the containers to your fleet in Boxtech and identify you as the BIC Code Holder and/or the Current Operator.  This file can include owned containers and leased containers in the same file.

### Update Container details 

In this case you would fill in all container details known to you \(more complete the better\) and upload using the **fleet in** feature.  If the container exists and you are the BIC Code Holder the container details will be updated according to your request.

If the containers are new to Boxtech they will be added using the details provided.

### 'On Hire' Containers to my fleet

In this case you would simply add the containers to the template and upload using the **fleet in** feature.  This will add the containers to your fleet in Boxtech and identify you as the Current Operator.

### 'Off Hire' Containers from my fleet

In this case you would simply add the containers to the template and upload using the **off hire** feature.  This will remove you from the Current Operator field in Boxtech.

### 'Off Hire' Leaseback containers

In this case use the **off hire** feature, this covers when the container is marked with your BIC Code but is returned to the lessor as although marked against your BIC Code it was on lease.  An alert will be raised to show this in Boxtech.

### Remove Containers from Fleet

You should use the sold or scrapped feature for this purpose, as you would know why and where the containers are leaving the fleet.  You can use the Fleet Out / Off Hire process if you are identifying containers in the same file that are being off hired or marked as sold or scrapped.

If you do not know where the containers are you can mark them as[ lost or stolen](container-alerts.md#lost) using an alert.

For leased containers use the off hire process

