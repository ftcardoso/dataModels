# Private Transportation

## Description

This entity model a particular private transportation trip, including all properties which can be used to characterize it.

## Data Model

- ```id```: Entity's unique identifier.

- ```type```: Entity type. It must be equal to ```PrivateTransportationTrip```.

- ```mode```: Describes the private transportation that was used.
	- Attribute type: [Text](https://schema.org/Text)
	- Allowed values:
		- ```Foot```
		- ```Car```
		- ```Bike```
	- Mandatory

- ```polyline```: A GeoJSON (multi)line string which defines this favorite trip segment.

        - Attribute type: geo:json.
        - Normative References: https://tools.ietf.org/html/rfc7946
        - Mandatory.

## Example
```
{
    "id": "PrivateTransportationTripID",
    "type": "PrivateTransportationTrip",
    "mode": "Car",
    "polyline": ""
}