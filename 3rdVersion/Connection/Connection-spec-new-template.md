# Connection

## Description

This entity contains a harmonised description of whose Person uses which Wearable.

## Data Model

The data model is defined as shown below:

-   `id` : Entity's unique identifier.

-   `type` : Entity type. It must be equal to `Wearable`.

-   `usedBy` : 
    -   Attribute type: Relationship. Reference to an entity of type `Person`.
    -   Mandatory

-   `usingWearable` : 
    -   Attribute type: Relationship. Reference to an entity of type `Sensor`.
    -   Mandatory

-   `connectionStartedAt` : 
    -   Attribute type: Property. [Date](https://schema.org/Date).
    -   Optional

-   `connectionFinishedAt` : 
    -   Attribute type: Property. [Date](https://schema.org/Date).
    -   Optional

-   `knowsAbout` : 
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
  "id": "urn:ngsi-ld:Wearable:003",
  "type": "Wearable",
    "hasBloodPressureSensor": {
        "type": "Relationship",
        "object": "urn:ngsi-ld:Sensor:005"
    },
    "hasHeartRateSensor": {
        "type": "Relationship",
        "object": "urn:ngsi-ld:Sensor:006"
    },
    "hasTemperatureSensor": {
        "type": "Relationship",
        "object": "urn:ngsi-ld:Sensor:007"
    },
    "hasOxygenSaturationSensor": {
        "type": "Relationship",
        "object": "urn:ngsi-ld:Sensor:008"
    },
    "knowsAbout": {
        "type": "Relationship",
        "object": "urn:ngsi-ld:Person:001"
    },
  "@context": [
    "https://raw.githubusercontent.com/rui-vp-fernandes/Fiware/main/context.jsonld",
    "https://uri.etsi.org/ngsi-ld/v1/ngsi-ld-core-context-v1.3.jsonld"
  ]
}
```
