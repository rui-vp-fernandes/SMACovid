# App

## Description

This entity contains a harmonised description of the information a Person defines using an app, to be delivered to a health monitoring system.

## Data Model

The data model is defined as shown below:

-   `id` : Entity's unique identifier.

-   `type` : Entity type. It must be equal to `App`.

-   `dyspnoea` : Status of the parking spot from the point of view of occupancy.

    -   Attribute type: Property. [Number](https://schema.org/Number)
    -   Metadata:
        -   `timestamp` : Timestamp which reflects the date when the attribute
            value was obtained.
            -   Type: [DateTime](https://schema.org/DateTime)
            -   Optional
        -   `unitCode` : Definition of used units for the attribute value.
            -   Type: [Text](https://schema.org/Text)
            -   Optional
    -   `TimeInstant` :
        [Timestamp](https://github.com/telefonicaid/iotagent-node-lib#TimeInstant)
        saved by FIWARE's IoT Agents. Note: This attribute has not been
        harmonized to keep backwards compatibility with current FIWARE reference
        implementations.
        -   Type: [DateTime](https://schema.org/DateTime). here can be
            production environmments where the attribute type is equal to the
            `ISO8601` string. If so, it must be considered as a synonym of
            `DateTime`.
        -   Optional
    -   Mandatory

-   `width` : Width of the parking spot.

    -   Attribute type: Property. [Number](https://schema.org/Number)
    -   Optional

-   `length` : Length of the parking spot.

    -   Attribute type: Property. [Number](https://schema.org/Number)
    -   Optional

-   `refParkingGroup` : Group to which the parking spot belongs to. For model
    simplification purposes only one group is allowed per parking spot.

    -   Attribute type: Relationship. Reference to an entity of type `ParkingGroup`.
    -   Optional

-   `refParkingSite` : Parking site to which the parking spot belongs to.

    -   Attribute type: Relationship. Reference to an entity of type `OnStreetParking` or type
        `OffStreetParking`, depending on the value of the `category` attribute.
    -   Mandatory

-   `category` : Category(ies) of the parking spot.

    -   Attribute type: Property. [Text](https://schema.org/Text)
    -   Allowed values:
        -   `onstreet` : The parking spot belongs to an onstreet parking site.
        -   `offstreet` : The parking spot belongs to an offstreet parking site.
        -   Other values as per application needs
    -   Mandatory

-   `TimeInstant` :
    [Timestamp](https://github.com/telefonicaid/iotagent-node-lib#TimeInstant)
    saved by FIWARE's IoT Agent. Note: This attribute has not been harmonized to
    keep backwards compatibility with current FIWARE reference implementations.

    -   Attribute type: Property. [DateTime](https://schema.org/DateTime). There can be
        production environmments where the attribute type is equal to the
        `ISO8601` string. If so, it must be considered as a synonym of
        `DateTime`.
    -   Optional

-   `refDevice` : The device representing the physical sensor used to monitor
    this parking spot.
    -   Attribute type: Relationship. Reference to entity of type
        [Device](../../../Device/Device/doc/spec.md)
    -   Optional

**Note**: JSON Schemas are intended to capture the data type and associated
constraints of the different Attributes, regardless their final representation
format in NGSI(v2, LD).

## Examples

### Normalized Example

Normalized NGSI response

```json
{
    "id": "santander:daoiz_velarde_1_5:3",
    "type": "ParkingSpot",
    "status": {
        "value": "free",
        "metadata": {
            "timestamp": {
                "type": "DateTime",
                "value": "2018-09-21T12:00:00"
            }
        }
    },
    "category": {
        "value": ["onstreet"]
    },
    "refParkingSite": {
        "type": "Relationship",
        "value": "santander:daoiz_velarde_1_5"
    },
    "name": {
        "value": "A-13"
    },
    "location": {
        "type": "geo:json",
        "value": {
            "type": "Point",
            "coordinates": [-3.80356167695194, 43.46296641666926]
        }
    }
}
```

### key-value pairs Example

Sample uses simplified representation for data consumers `?options=keyValues`

```json
{
    "id": "santander:daoiz_velarde_1_5:3",
    "type": "ParkingSpot",
    "name": "A-13",
    "location": {
        "type": "Point",
        "coordinates": [-3.80356167695194, 43.46296641666926]
    },
    "status": "free",
    "category": ["onstreet"],
    "refParkingSite": "santander:daoiz_velarde_1_5"
}
```

### LD Example

Sample uses the NGSI-LD representation

```json
{
    "id": "urn:ngsi-ld:ParkingSpot:santander:daoiz_velarde_1_5:3",
    "type": "ParkingSpot",
    "status": {
        "type": "Property",
        "value": "free",
        "observedAt": "2018-09-21T12:00:00Z"
    },
    "category": {
        "type": "Property",
        "value": ["onstreet"]
    },
    "refParkingSite": {
        "type": "Relationship",
        "object": "urn:ngsi-ld:ParkingSite:santander:daoiz_velarde_1_5"
    },
    "name": {
        "type": "Property",
        "value": "A-13"
    },
    "location": {
        "type": "GeoProperty",
        "value": {
            "type": "Point",
            "coordinates": [-3.80356167695194, 43.46296641666926]
        }
    },
    "@context": [
        "https://schema.lab.fiware.org/ld/context",
        "https://uri.etsi.org/ngsi-ld/v1/ngsi-ld-core-context.jsonld"
    ]
}
```
