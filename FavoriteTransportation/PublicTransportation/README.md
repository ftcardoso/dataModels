# Public Transportation data model

The Service Network defines a set of data models with the main purpose of collecting information about the trips made by users of the public transportation services. This way, it is possible to map the user's trips and collect useful information regarding their habits when using public transportation, such as the most used stops, the most used types of transports, and other useful metrics. 
The data models described below are the Trip, Stop, Route and Agency entities, which interact in a hierarchical way in order to map the user's trips of a service network.
These data models were defined based on the General Transit Feed Specification [6], which is a standard that defines a common format for public transportation schedules and associated geographic information, based on CSV files. It is one of the most popular and used standards for public transportation [10], with many entities already using it to describe their services. This means there is a lot of data already available, and there are many applications developed using this standard. These facts lead to the adoption of this standard as the base of the models defined here. 

This folder contains all the entities related to the Service Network data model:

* `Trip` - This entity model a particular trip model, including all properties which can be used to characterize trips from public transport service networks. 
* `Agency` - This entity model a particular a public transport agency model, including all properties which are commom to multiple trip instances belonging to such model.
* `Route` - This entity model a particular a public transport route model, including all properties which are commom to multiple trip instances belonging to such model.
* `Stop` - This entity model a particular a public transport stop model, including all properties which are commom to multiple trip instances belonging to such model.