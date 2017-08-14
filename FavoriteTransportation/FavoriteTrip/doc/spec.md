# Favorite Trip

## Description

This entity model a particular favorite trip, including all properties which can be used to characterize it. The favorite trip includes severall segments that together complete the trip. Each one of them can be done using public or private transportation.

## Data Model

- ```id```: Entity's unique identifier.

- ```type```: Entity type. It must be equal to ```FavoriteTrip```.

- ```fromPlace```: Location where the trip starts represented by a GeoJSON Point.
    - Attribute type: ``geo_json`` 
	- Normative References: https://tools.ietf.org/html/rfc7946
	- Mandatory

- ```toPlace```: Location where the trip stops represented by a GeoJSON Point.
    - Attribute type: ``geo_json`` 
	- Normative References: https://tools.ietf.org/html/rfc7946
	- Mandatory

- ```segments```: An a array of segments containing details(see list below) about each segment that completes the favorite trip. Each trip can have one or more segments.
	- Attribute type: List 

    - ```id```: Entity's unique identifier.
    - ```type```: Refers to the type of transportation used (public or private).
        - Attribute type: [Text](https://schema.org/Text)
        - Allowed values:
            - ```public```
            - ```private```
        - Mandatory
    - ```transporation```: Reference to a [Private]() or [Public]() transportation.
        - Mandatory

   

## Example
```
{
    "id": "favoritetripID",
    "type": "FavoriteTrip",
    "fromPlace": "",
    "toPlace": ""
    "segments": [
    	"segment1":{
            "id": "segmentID",
            "type": "public"
            "transportation": "PublicTransportationTripID"
        }
    ]
}
```