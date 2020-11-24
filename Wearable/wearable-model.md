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
      - description: Measured arterial pressure
    - oxygenSaturation:
      - x-ngsi:
        - type: "Property"
        - model: "https://schema.org/Integer"
      - type: "integer"
      - format: "int32"
      - description: Measured oxygen saturation
    - temperature:
      - x-ngsi:
        - type: "Property"
        - model: "http://www.w3.org/2001/XMLSchema#double"
      - type: "double"
      - description: Measured temperature
    - heartRate:
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
