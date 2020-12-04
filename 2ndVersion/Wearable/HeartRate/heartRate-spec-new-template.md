# HeartRate

## Description

This entity contains a harmonised description of the heart rate measurements a wearable device can deliver to a health monitoring system.

## Data Model

The data model is defined as shown below:

-   `id` : Entity's unique identifier.

-   `type` : Entity type. It must be equal to `HeartRate`.

-   `heartRate` : Measured heart rate by the wearable device.
    -   Attribute type: Property. [Number](https://schema.org/Number)
    -   Metadata:
        -   `timestamp` : Timestamp which reflects the date when the attribute
            value was obtained.
            -   Type: [DateTime](https://schema.org/DateTime)
            -   Optional
        -   `unitCode` : Definition of used units for the attribute value.
            -   Type: [Text](https://schema.org/Text)
            -   Optional
    -   Mandatory

-   `hasInfoAbout` : 
    -   Attribute type: Relationship. Reference to an entity of type `Person`.
    -   Optional



**Note**: JSON Schemas are intended to capture the data type and associated
constraints of the different Attributes, regardless their final representation
format in NGSI(v2, LD).

## Examples

### LD Example

Sample uses the NGSI-LD representation

```json
{
  "id": "urn:ngsi-ld:HeartRate:002",
  "type": "Wearable",
  "bloodPressure": {
    "type": "Property",
    "value": 120,
    "observedAt": "2020-11-22T12:28:00Z",
    "unitCode": "HN"
  },
  "oxygenSaturation": {
    "type": "Property",
    "value": 98,
    "observedAt": "2020-11-22T12:28:00Z",
    "unitCode": "C62"
  },
  "temperature": {
    "type": "Property",
    "value": 35,
    "observedAt": "2020-11-22T12:28:00Z",
    "unitCode": "CEL"
  },
  "heartRate": {
    "type": "Property",
    "value": 65,
    "observedAt": "2020-11-22T12:28:00Z",
    "unitCode": "C62"
  },
  "isOwnedBy": {
    "type": "Relationship",
    "object": "urn:ngsi-ld:Person:001"
  },
  "@context": [
    "https://raw.githubusercontent.com/rui-vp-fernandes/Fiware/main/context.jsonld",
    "https://uri.etsi.org/ngsi-ld/v1/ngsi-ld-core-context-v1.3.jsonld"
  ]
}
```
