Wearable:
  - required:
    - {{A VER DEPOIS}}
    
  - type: "object"
  
  ## Description
  This entity contains a harmonised description of the measurements a wearable device can deliver to a health monitoring system.
        
        
  ## Data Model
      
  - properties:  
    - bloodPressure:
      - x-ngsi:
        - type: "Property"
        - model: "https://schema.org/Integer"
      - type: "integer"
      - format: "int32"
      -   Metadata:
          -   `timestamp` : Timestamp which reflects the date when the attribute
              value was obtained.
              -   Type: [DateTime](https://schema.org/DateTime)
              -   Optional
          -   `unitCode` : Definition of used units for the attribute value.
              -   Type: [DateTime](https://schema.org/DateTime)
              -   Optional
      - description: Measured arterial pressure by the wearable device
    - oxygenSaturation:
      - x-ngsi:
        - type: "Property"
        - model: "https://schema.org/Integer"
      - type: "integer"
      - format: "int32"
      -   Metadata:
          -   `timestamp` : Timestamp which reflects the date when the attribute
              value was obtained.
              -   Type: [DateTime](https://schema.org/DateTime)
              -   Optional
          -   `unitCode` : Definition of used units for the attribute value.
              -   Type: [DateTime](https://schema.org/DateTime)
              -   Optional
      - description: Measured oxygen saturation by the wearable device
    - temperature:
      - x-ngsi:
        - type: "Property"
        - model: "http://www.w3.org/2001/XMLSchema#double"
      - type: "double"
      -   Metadata:
          -   `timestamp` : Timestamp which reflects the date when the attribute
              value was obtained.
              -   Type: [DateTime](https://schema.org/DateTime)
              -   Optional
          -   `unitCode` : Definition of used units for the attribute value.
              -   Type: [DateTime](https://schema.org/DateTime)
              -   Optional
      - description: Measured temperature by the wearable device
    - heartRate:
      - x-ngsi:
        - type: "Property"
        - model: "https://schema.org/Integer"
      - type: "integer"
      - format: "int32"
      -   Metadata:
          -   `timestamp` : Timestamp which reflects the date when the attribute
              value was obtained.
              -   Type: [DateTime](https://schema.org/DateTime)
              -   Optional
          -   `unitCode` : Definition of used units for the attribute value.
              -   Type: [DateTime](https://schema.org/DateTime)
              -   Optional
      - description: Measured heart rate by the wearable device
    - isOwnedBy:
      - x-ngsi:
        - type: "Relationship"
        - model: "https://schema.org/URL"
      - type: "string"
      - format: "URL"
      -   Metadata:
          -   `timestamp` : Timestamp which reflects the date when the attribute
              value was obtained.
              -   Type: [DateTime](https://schema.org/DateTime)
              -   Optional
          -   `unitCode` : Definition of used units for the attribute value.
              -   Type: [DateTime](https://schema.org/DateTime)
              -   Optional
      - description: Identifies the Person using the wearable



  ## Examples of use

  ### LD Example

```json
  {
      "id": "urn:ngsi-ld:Wearable:002",
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


  ## Use it with a real service

  {{Provide a link to a real service providing data following the harmonized data format}}

  ## Open Issues

  {{Describe here any open issue}}
