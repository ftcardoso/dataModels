# Service Alert

## Description
This enity model a particular public transport service alert model, including all properties which can be used to specify a public transport service alert whenever there is a disruption on the public transport network. This data model is based on the [Realtime Transit Service Alerts](https://developers.google.com/transit/gtfs-realtime/guides/service-alerts) that defines a common format for public transportation service alerts.

## Data Model

- ```id```: Entity's unique identifier.

- ```type```: Entity type. It must be equal to ```Alert```.

- ```header```: Summary of the alert.
	- Attribute type: [Text](https://schema.org/Text)
	- Mandatory

- ```description```: A complete description of the alert.
	- Attribute type: [Text](https://schema.org/Text)
	- Mandatory

- ```timeRange```: The time range that the alert will be active. The time range can refer to one or multiple time ranges. It's represented as an array of arrays, where the first position refers to the start date and the second to the end date of the time range.
	- Attribute type: List
	- Mandatory

- ```refEntity```: Specify exactly which parts of the network this alert affetcs.
	- Attribute type: List of references to entities of type [Entity](https://github.com/ftcardoso/dataModels/blob/public_transportation_2/Transportation/PublicTransportServiceAlerts/Entity/doc/spec.md)
	- Mandatory

- ```cause```: The cause of the alert. Can only exist one cause for each alert.
	- Attribute type: [Text](https://schema.org/Text)
	- Allowed Values:
		- ```Unknown cause```
		- ```Other cause (not represented by any of these option)```
		- ```Technical problem```
		- ```Demonstration```
		- ```Accident```
		- ```Holiday```
		- ```Weather```
		- ```Maintenance```
		- ```Construction```
		- ```Police activity```
		- ```Medical emergency```
	- Mandatory

- ```effect```: What effect does this problem have on the specified entity. Cal only exist one effect for each alert.
	- Attribute type: [Text](https://schema.org/Text)
	- Allowed values:
		- ```No service```
		- ```Reduced service```
		- ```Significant delays```
		- ```Detour```
		- ```Additional service```
		- ```Modified service```
		- ```Stop moved```
		- ```Other effet```
		- ```Unknown effect```
	- Mandatory

- ```dateModified```: Last update timestamp of this entity.
	- Attribute type: [DateTime](https://schema.org/DateTime)
	- Optional

- ```dateCretated```: Creation timestamp of this entity.
	- Attribute type: [DateTime](https://schema.org/DateTime)
    - Optional


## Example

```
{
    "id": "Alert0000",
    "type": "Alert",
    "header": "Holiday",
    "description": "Complete description of what will happen",
    "timeRange": [
    	[
            2017-04-05T08:15:30+01:00,
            2017-04-06T08:15:30+01:00
        ],
        [
            2017-04-08T08:15:30+01:00,
            2017-04-09T08:15:30+01:00
        ]
    ],
    "refEntity": ["entityID0"],
    "cause": "Holiday",
    "effect": "Modified Service"
}
```
