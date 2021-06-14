---
layout: default
title: SOLAS VGM
parent: Use Cases
---

# SOLAS VGM Process

BoxTech allows shippers, carriers, terminals, depots, and other supply chain participants to instantly obtain technical information about containers, such as tare weight, size/type and maximum gross mass.

BoxTech means a one-stop-shop to obtain container tare weights for use in Method 2 SOLAS VGM calculations.

To obtain the tare weight for a given containers

**Query the API**

```text
https://app.bic-boxtech.org/api/v2.0/container/GLDU5334260
```

_Note: You will need to provide the bearer in the header as described in the_ [_guide_](vgm.md) _with your token_

**Examine the Results**

Look for the `tare_kg` in the json response, you can now use this value in your SOLAS VGM method 2 calculations.

```text
{
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
   }
```

