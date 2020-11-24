App:
  - required:
    - {{A VER DEPOIS}}
    
  - type: "object"
  
  ## Description
  This entity contains a harmonised description of the information a Person defines using an app, to be delivered to a health monitoring system.
        
        
  ## Data Model
      
  - properties:  
    - dyspnoea:
      - x-ngsi:
        - type: "Property"
        - model: "http://www.w3.org/2001/XMLSchema#boolean"
      - type: "boolean"
      - description: Measured arterial pressure
    - cough:
      - x-ngsi:
        - type: "Property"
        - model: "http://www.w3.org/2001/XMLSchema#boolean"
      - type: "boolean"
      - description: Measured oxygen saturation
    - anosmia:
      - x-ngsi:
        - type: "Property"
        - model: "http://www.w3.org/2001/XMLSchema#boolean"
      - type: "boolean"
      - description: Measured temperature
    - contactCovid:
      - x-ngsi:
        - type: "Property"
        - model: "http://www.w3.org/2001/XMLSchema#boolean"
      - type: "boolean"
      - description: Number of floors above ground within the building
    - diarrhea:
      - x-ngsi:
        - type: "Property"
        - model: "https://schema.org/Integer"
      - type: "integer"
      - format: "int32"
      - description: Number of floors above ground within the building
    - isOwnedBy:
      - x-ngsi:
        - type: "Relationship"
        - model: "https://schema.org/URL"
      - type: "string"
      - format: "URL"
      - description: Identifies the Person using the wearable

  ## Examples of use

  ### LD Example


  ## Use it with a real service

  {{Provide a link to a real service providing data following the harmonized data format}}

  ## Open Issues

  {{Describe here any open issue}}
