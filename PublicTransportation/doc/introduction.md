# Public Transportation Harmonized Data Models

These data models describe entities useful for dealing with public transportation data. These entities are primarily
associated with vertical segments of Public Transportation data and Smart Cities.

The main entities identified are:

### VehiclePosition:

+ [PublicVehicle](../VehiclePosition/PublicVehicle/doc/spec.md). It represents the current position of a specific public transportation vehicle. 
+ [PublicVehicleModel](../VehiclePosition/PublicVehicleModel/doc/spec.md). It represents a specific type o vehicle.

### ServiceAlert:

+ [Alert](../ServiceAlert/Alert/doc/spec.md). It represents a service alert related to public transportation network.
+ [Entity](../ServiceAlert/Entity/doc/spec.md). It represents the entity that the alert is related.
+ [TimeRange](../ServiceAlert/TimeRange/doc/spec.md). It represents the alert time range.

### VehicleTrip:

+ [Trip](../VehicleTrip/Trip/doc/spec.md). It represents a trip for a public transportation vehicle.
+ [Agency](../VehicleTrip/Agency/doc/spec.md). It represents the agency that the trip is related.
+ [Route](../VehicleTrip/Route/doc/spec.md). It represents the route that the trip belongs.
+ [Stop](../VehicleTrip/Stop/doc/spec.md). It represents the stops that are part of the trip.