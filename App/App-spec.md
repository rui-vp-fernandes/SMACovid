## Description
This entity contains a harmonised description of the information a Person defines using an app, to be delivered to a health monitoring system.
        
        
## Data Model
      
- properties:  
  - dyspnoea:
      - x-ngsi:
        - type: "Property"
        - model: "http://www.w3.org/2001/XMLSchema#boolean"
      - type: "boolean"
      - description: Identification of dyspnoea existence
    - cough:
      - x-ngsi:
        - type: "Property"
        - model: "http://www.w3.org/2001/XMLSchema#boolean"
      - type: "boolean"
      - description: Identification of cough existence
    - anosmia:
      - x-ngsi:
        - type: "Property"
        - model: "http://www.w3.org/2001/XMLSchema#boolean"
      - type: "boolean"
      - description: Identification of anosmia existence
    - contactCovid:
      - x-ngsi:
        - type: "Property"
        - model: "http://www.w3.org/2001/XMLSchema#boolean"
      - type: "boolean"
      - description: Identification of contact with a COVID-19 infected person 
    - diarrhea:
      - x-ngsi:
        - type: "Property"
        - model: "https://schema.org/Integer"
      - type: "integer"
      - format: "int32"
      - description: Number of times the person suffered from diarrhea during the present day
    - isOwnedBy:
      - x-ngsi:
        - type: "Relationship"
        - model: "https://schema.org/URL"
      - type: "string"
      - format: "URL"
      - description: Identifies the Person using the wearable

  ## Examples of use

  ### LD Example

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


  ## Use it with a real service

  {{Provide a link to a real service providing data following the harmonized data format}}

  ## Open Issues

  {{Describe here any open issue}}
