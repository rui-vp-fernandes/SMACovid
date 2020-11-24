# App

## Description

This entity contains a harmonised description of the information a Person defines using an app, to be delivered to a health monitoring system.

## Data Model

The data model is defined as shown below:

-   `id` : Entity's unique identifier.

-   `type` : Entity type. It must be equal to `App`.

-   `dyspnoea` : Identification of dyspnoea existence.
    -   Attribute type: Property. [Boolean](http://www.w3.org/2001/XMLSchema#boolean)
    -   Mandatory

-   `cough` : Identification of cough existence.
    -   Attribute type: Property. [Boolean](http://www.w3.org/2001/XMLSchema#boolean)
    -   Mandatory

-   `anosmia` : Identification of anosmia existence.
    -   Attribute type: Property. [Boolean](http://www.w3.org/2001/XMLSchema#boolean)
    -   Mandatory

-   `contactCovid` : Identification of contact with a COVID-19 infected person.
    -   Attribute type: Property. [Boolean](http://www.w3.org/2001/XMLSchema#boolean)
    -   Mandatory

-   `diarrhea` : Number of times the person suffered from diarrhea during the present day.
    -   Attribute type: Property. [Number](https://schema.org/Number)
    -   Mandatory

-   `hasInfoAbout` : Identifies the Person using the wearable.
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
  "id": "urn:ngsi-ld:App:001",
  "type": "App",
  "dyspnoea": {
    "type": "Property",
    "value": true
  },
  "cough": {
    "type": "Property",
    "value": true
  },
  "anosmia": {
    "type": "Property",
    "value": false
  },
  "contactCovid": {
    "type": "Property",
    "value": false
  },
  "diarrhea": {
    "type": "Property",
    "value": 3
  },
  "hasInfoAbout": {
    "type": "Relationship",
    "object": "urn:ngsi-ld:Person:001"
  },
  "@context": [
    "https://raw.githubusercontent.com/rui-vp-fernandes/Fiware/main/context.jsonld",
    "https://uri.etsi.org/ngsi-ld/v1/ngsi-ld-core-context-v1.3.jsonld"
  ]
}
```
