# API Use Case Examples

## SOLAS VGM

BoxTech allows shippers, carriers, terminals, depots, and other supply chain participants to instantly obtain technical information about containers, such as tare weight, size/type and maximum gross mass. BoxTech means a one-stop-shop to obtain container tare weights for use in Method 2 SOLAS VGM calculations.

To obtain the tare weight for a given containers you would use the GET method below to retrieve the container detail and would look for the `tare_kg` in the response, you can now use this in your SOLAS VGM method 2 calculations

## Terminal Process

BoxTech allows shippers, carriers, terminals, depots, and other supply chain participants to instantly obtain technical information about containers, such as tare weight, size/type and maximum gross mass.

BoxTech means a one-stop-shop to obtain container max weights for your automated safety checks within a terminal.

For safety you may want to obtain the max weight for a given container to cross check the weight of a container on arrival at the port or terminal.

To obtain the tare weight for a given containers you would use the GET method below to retrieve the container detail and would look for the `max_payload_kg` or for the loading process the `max_gross_mass_kg` in the response

## Query the API

{% swagger baseUrl="https://app.bic-boxtech.org/api" path="/v2.0/container/:container" method="get" summary="GET Container Detail" %}
{% swagger-description %}
Find the technical Details for a given container number
{% endswagger-description %}

{% swagger-parameter name="container" type="string" required="true" in="path" %}
Container Number i.e. GLDU5334260
{% endswagger-parameter %}

{% swagger-response status="200" description="" %}
```
[{
       "uploaderaccountname": "TOUAX",
       "bic_code": "GLDU",
       "prefix": "GLD",
       "equipment_identifier": "U",
       "serial_number": "533426",
       "check_digit": "0",
       "group_st": "20DC",
       "detail_st": null,
       "tare_kg": 2230,
       "tare_lbs": 4920,
       "max_payload_kg": 30480,
       "max_payload_lbs": 67200,
       "max_gross_mass_kg": 28250,
       "max_gross_mass_lbs": 62280,
       "cubic_capacity_cbm": 33,
       "cubic_capacity_cuft": 1170,
       "stacking_kg": 216000,
       "stacking_lbs": 476190,
       "racking_kg": null,
       "racking_lbs": null,
       "racking_n": null,
       "one_door_off_stacking_kg": null,
       "one_door_off_stacking_lbs": null,
       "one_door_off_racking_kg": null,
       "one_door_off_racking_lbs": null,
       "one_door_off_racking_n": null,
       "one_door_off_end_wall_strength_kg": null,
       "one_door_off_end_wall_strength_lbs": null,
       "manufacture_number": null,
       "manufacture_date": "2008-03-27T00:00:00.000Z",
       "manufacturer": "CIMCDCMCDALIAN",
       "customs_approval": null,
       "customs_approval_type": null,
       "csc_approval": null,
       "timber_treatment_approval": null,
       "external_length_mm": null,
       "external_width_mm": null,
       "external_height_mm": null,
       "internal_length_mm": null,
       "internal_width_mm": null,
       "internal_height_mm": null,
       "door_opening_width_mm": null,
       "door_opening_height_mm": null,
       "codeholder": "TOUAX",
       "container_number": "GLDU5334260",
       "checkDigitwarning": false,
       "external_length_ft": null,
       "internal_length_ft": null,
       "external_width_ft": null,
       "internal_width_ft": null,
       "external_height_ft": null,
       "internal_height_ft": null,
       "door_opening_width_ft": null,
       "door_opening_height_ft": null
   }]
```
{% endswagger-response %}
{% endswagger %}

### Retrieve the Tare Weight from Response

Look for the \`tare\_kg\` in the json response, you can now use this value in your SOLAS VGM method 2 calculations.

```
[{
       "uploaderaccountname": "TOUAX",
       "bic_code": "GLDU",
       "prefix": "GLD",
       "equipment_identifier": "U",
       "serial_number": "533426",
       "check_digit": "0",
       "group_st": "20DC",
       "detail_st": null,
       "tare_kg": 2230,
       "tare_lbs": 4920,
       "max_payload_kg": 30480,
       "max_payload_lbs": 67200,
       "max_gross_mass_kg": 28250,
       "max_gross_mass_lbs": 62280,
       "cubic_capacity_cbm": 33,
       "cubic_capacity_cuft": 1170,
       "stacking_kg": 216000,
       "stacking_lbs": 476190,
       "racking_kg": null,
       "racking_lbs": null,
       "racking_n": null,
       "one_door_off_stacking_kg": null,
       "one_door_off_stacking_lbs": null,
       "one_door_off_racking_kg": null,
       "one_door_off_racking_lbs": null,
       "one_door_off_racking_n": null,
       "one_door_off_end_wall_strength_kg": null,
       "one_door_off_end_wall_strength_lbs": null,
       "manufacture_number": null,
       "manufacture_date": "2008-03-27T00:00:00.000Z",
       "manufacturer": "CIMCDCMCDALIAN",
       "customs_approval": null,
       "customs_approval_type": null,
       "csc_approval": null,
       "timber_treatment_approval": null,
       "external_length_mm": null,
       "external_width_mm": null,
       "external_height_mm": null,
       "internal_length_mm": null,
       "internal_width_mm": null,
       "internal_height_mm": null,
       "door_opening_width_mm": null,
       "door_opening_height_mm": null,
       "codeholder": "TOUAX",
       "container_number": "GLDU5334260",
       "checkDigitwarning": false,
       "external_length_ft": null,
       "internal_length_ft": null,
       "external_width_ft": null,
       "internal_width_ft": null,
       "external_height_ft": null,
       "internal_height_ft": null,
       "door_opening_width_ft": null,
       "door_opening_height_ft": null,
       "capacity_litres": "31200",
       "imdg_code": "T1",
       "adr_rid_code": "L10CH",
       "baffles": false
   }]
```
