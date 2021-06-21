# Boxtech Dataset

Boxtech stores a number of data elements about a container, the details of which can be found below.

## BIC Code Holder and Current Operator

There are two parties that are often required to be known for a container, and these are the definitions and how they are determined:

### BIC Code Holder

The owner of the BIC Prefix that is marked on the container, this company hold an account with BIC and are the registered code holder.  This could be for example a lessor, carrier or shipper with own containers.

### Current Operator

If the container is marked with a BIC prefix belonging to a lessor, they may not be the current operator of the container, as it will likely be 'on hire' to another company.  When an `uploader` provides their fleet to Boxtech, if they are not the BIC Code Holder they will become the current operator, when they off hire OR another company on hires and uploads their fleet they will be removed and the new operator added.  

## Physical Characteristics 

The Physical Characteristics are the details that are marked on the container as per ISO6346

`Group ST` is the ISO Container Group Type Code as detailed in ISO6346, where this is not provided by the uploader it is determined from the `Detail ST` 

`Detail ST` is the ISO Container Detail Type Code as detailed in ISO6346

`Tare Weight` is the Tare Weight of the container, detailed in kgs and lbs.  

`Max Payload` is the maximum weight of the goods that can be loaded in the container, detailed in kgs and lbs. 

`Max Gross` is the maximum weight that the container including its own weight and the weight of the goods can safely contain.  This weight should not be exceeded.  Detailed in kgs and lbs.  

`Stacking` is the weight that ..

`Racking` is the weight that ...

`Cubic Capacity` is the volume that the container has capacity for internal storage.  Detailed in m3 and cuft. 

## Dimensions 

Note that were the dimensions are not provided on upload for the external measurements they are provided under ISO6346 for the container type, where available.  Internal measurements are only provided by the uploader.

`External Length` - The length of the container measured from the outside.  Detailed in mm and ft.

`External Width` - The width of the container measured from the outside.  Detailed in mm and ft.

`External Height` - The height of the container measured from the outside.  Detailed in mm and ft.

`Internal Length` - The length of the container measured from the inside.  Detailed in mm and ft.

`Internal Width` - The width of the container measured from the inside.  Detailed in mm and ft.

`Internal Height` - The height of the container measured from the inside.  Detailed in mm and ft.

`Door Opening Width` - 

`Door Opening Height` - 

## One Door Off Operations 

`Stacking` - 

`Racking` - 

`End Wall Strength` - 

## Manufacturer Data and Data Plates

`Manufacturer` - Name of the Manufacturer of the container

`Manufacturer #` - identification code of the manufacturer

`Manufacturing Date` - Date the container was manufactured 

`CSC Approval` - 

`Customs Approval`

`Customs Approval Type`

`Timber Treatment Plate` - 

## Conversions

### Weights \(kgs/lbs\)

Where the weight of a container is provided in only 1 of the unit types, it will be calculated for the other using the following calculation.

 `LBS / 2.20462 = KGS`

 `KGS * 2.20462 = LBS`

### Volume \(m3, cuft\)

Where the volume of a container is provided in only 1 of the unit types, it will be calculated for the other using the following calculation.

`CBM * 35.3146667 = CUFT`

`CUFT / 35.3146667 = CBM`

