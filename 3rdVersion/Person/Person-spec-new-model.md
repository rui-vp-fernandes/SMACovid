# Person

## Description

This entity contains a harmonised description of the information about a Person using a health monitoring system.

## Data Model

The data model is defined as shown below:

-   `id` : Entity's unique identifier.

-   `type` : Entity type. It must be equal to `Person`.

-   `givenName` : Person's first name.
    -   Attribute type: Property. [Text](https://schema.org/Text)
    -   Mandatory

-   `familyName` : Person's last name.
    -   Attribute type: Property. [Text](https://schema.org/Text)
    -   Mandatory

-   `gender` : Person's gender. One of two possibilities: "Female", "Male".
    -   Attribute type: Property. [Text](https://schema.org/Text)
    -   Mandatory

-   `age` : Person's age.
    -   Attribute type: Property. [Number](https://schema.org/Number)
    -   Mandatory

-   `height` : Person's height, in [cm].
    -   Attribute type: Property. [Number](https://schema.org/Number)
    -   Mandatory

-   `weight` : Person's weight, in [kg].
    -   Attribute type: Property. [Number](https://schema.org/Number)
    -   Mandatory

-   `fitbitId` : Code identifier of the Person's fitbit account.
    -   Attribute type: Property. [Text](https://schema.org/Text)
    -   Mandatory

-   `hasApp` : Identifies the App used by the Person.
    -   Attribute type: Relationship. Reference to an entity of type `App`.
    -   Mandatory

-   `hasWearable` : Identifies the wearable being used by the Person.
    -   Attribute type: Relationship. Reference to an entity of type `Wearable`.
    -   Mandatory



**Note**: JSON Schemas are intended to capture the data type and associated
constraints of the different Attributes, regardless their final representation
format in NGSI(v2, LD).

## Examples

### LD Example

Sample uses the NGSI-LD representation

```json
{
  "id": "urn:ngsi-ld:Person:015",
  "type": "Person",
  "givenName": {
    "type": "Property",
    "value": "Manuel"
  },
  "familyName": {
    "type": "Property",
    "value": "Oliveira"
  },
  "gender": {
    "type": "Property",
    "value": "Male"
  },
  "age": {
    "type": "Property",
    "value": 33
  },
  "height": {
    "type": "Property",
    "value": 175
  },
  "weight": {
    "type": "Property",
    "value": 73
  },
  "fitbitId": {
    "type": "Property",
    "value": 73
  },
  "hasApp": {
    "type": "Relationship",
    "object": "urn:ngsi-ld:App:003"
  },
  "hasWearable": {
    "type": "Relationship",
    "object": "urn:ngsi-ld:Wearable:005"
  },
  "@context": [
    "https://raw.githubusercontent.com/rui-vp-fernandes/Fiware/main/context.jsonld",
    "https://uri.etsi.org/ngsi-ld/v1/ngsi-ld-core-context-v1.3.jsonld"
  ]
}
```
