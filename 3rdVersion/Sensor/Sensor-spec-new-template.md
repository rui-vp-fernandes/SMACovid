# Sensor

## Description

This entity contains a harmonised description of a generic sensor data gathering structure. This allows its usage for all sensor read variables within the SMACovid application.

## Data Model

The data model is defined as shown below:

-   `id` : Entity's unique identifier.

-   `type` : Entity type. It must be equal to `Sensor`.

-   `measurementType` : Identification of the measured variable by the wearable device.
    -   Attribute type: Property. [Text](https://schema.org/Text)
    -   Mandatory

-   `sensorValue` : Measured value.
    -   Attribute type: Property. [Number](https://schema.org/Number)
    -   Mandatory

-   `obsTime` : 
    -   Attribute type: Property. [Date](https://schema.org/Date)
    -   Optional



**Note**: JSON Schemas are intended to capture the data type and associated
constraints of the different Attributes, regardless their final representation
format in NGSI(v2, LD).

## Examples

### LD Example

Sample uses the NGSI-LD representation

```json
{
  "id": "urn:ngsi-ld:Sensor:005",
  "type": "Sensor",
  "measurementType": 
    "type": "Property",
    "value": "heartRate",
  },
  "sensorValue": {
    "type": "Property",
    "value": 78,
  },
  "obsTime": {
    "type": "Property",
    "value": "2020-11-22T12:28:00Z",
  },
  "@context": [
    "https://raw.githubusercontent.com/rui-vp-fernandes/Fiware/main/context.jsonld",
    "https://uri.etsi.org/ngsi-ld/v1/ngsi-ld-core-context-v1.3.jsonld"
  ]
}
```
