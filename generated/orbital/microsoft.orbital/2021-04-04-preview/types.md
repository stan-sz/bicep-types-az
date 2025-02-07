# Microsoft.Orbital @ 2021-04-04-preview

## Resource Microsoft.Orbital/contactProfiles@2021-04-04-preview
* **Valid Scope(s)**: ResourceGroup
### Properties
* **apiVersion**: '2021-04-04-preview' (ReadOnly, DeployTimeConstant): The resource api version
* **etag**: string (ReadOnly): A unique read-only string that changes whenever the resource is updated.
* **id**: string (ReadOnly, DeployTimeConstant): The resource id
* **location**: string (Required): The geo-location where the resource lives
* **name**: string (Required, DeployTimeConstant): The resource name
* **properties**: [ContactProfilesProperties](#contactprofilesproperties): List of Contact Profile Resource Properties.
* **systemData**: [SystemData](#systemdata) (ReadOnly): Metadata pertaining to creation and last modification of the resource.
* **tags**: [TrackedResourceTags](#trackedresourcetags): Resource tags.
* **type**: 'Microsoft.Orbital/contactProfiles' (ReadOnly, DeployTimeConstant): The resource type

## Resource Microsoft.Orbital/spacecrafts@2021-04-04-preview
* **Valid Scope(s)**: ResourceGroup
### Properties
* **apiVersion**: '2021-04-04-preview' (ReadOnly, DeployTimeConstant): The resource api version
* **etag**: string (ReadOnly): A unique read-only string that changes whenever the resource is updated.
* **id**: string (ReadOnly, DeployTimeConstant): The resource id
* **location**: string (Required): The geo-location where the resource lives
* **name**: string (Required, DeployTimeConstant): The resource name
* **properties**: [SpacecraftsProperties](#spacecraftsproperties): List of Spacecraft Resource Properties.
* **systemData**: [SystemData](#systemdata) (ReadOnly): Metadata pertaining to creation and last modification of the resource.
* **tags**: [TrackedResourceTags](#trackedresourcetags): Resource tags.
* **type**: 'Microsoft.Orbital/spacecrafts' (ReadOnly, DeployTimeConstant): The resource type

## Resource Microsoft.Orbital/spacecrafts/contacts@2021-04-04-preview
* **Valid Scope(s)**: ResourceGroup
### Properties
* **apiVersion**: '2021-04-04-preview' (ReadOnly, DeployTimeConstant): The resource api version
* **etag**: string (ReadOnly): A unique read-only string that changes whenever the resource is updated.
* **id**: string (ReadOnly, DeployTimeConstant): The resource id
* **name**: string (Required, DeployTimeConstant): The resource name
* **properties**: [ContactsProperties](#contactsproperties): Properties of the Contact Resource.
* **systemData**: [SystemData](#systemdata) (ReadOnly): Metadata pertaining to creation and last modification of the resource.
* **type**: 'Microsoft.Orbital/spacecrafts/contacts' (ReadOnly, DeployTimeConstant): The resource type

## Function listAvailableContacts (Microsoft.Orbital/spacecrafts@2021-04-04-preview)
* **Resource**: Microsoft.Orbital/spacecrafts
* **ApiVersion**: 2021-04-04-preview
* **Input**: [ContactParameters](#contactparameters)
* **Output**: [AvailableContactsListResult](#availablecontactslistresult)

## ContactProfilesProperties
### Properties
* **autoTrackingConfiguration**: 'disabled' | 'sBand' | 'xBand': Auto track configuration.
* **eventHubUri**: string: The URI of the Event Hub used for telemetry
* **links**: [ContactProfileLink](#contactprofilelink)[] (Required): Links of the Contact Profile
* **minimumElevationDegrees**: int: Minimum viable elevation for the contact in decimal degrees.
* **minimumViableContactDuration**: string: Minimum viable contact duration in ISO 8601 format.

## ContactProfileLink
### Properties
* **channels**: [ContactProfileLinkChannel](#contactprofilelinkchannel)[] (Required): Contact Profile Link Channel
* **direction**: 'downlink' | 'uplink' (Required): Direction (uplink or downlink)
* **eirpdBW**: int: Effective Isotropic Radiated Power (EIRP) in dBW.
* **gainOverTemperature**: int: Gain To Noise Temperature in db/K.
* **polarization**: 'LHCP' | 'RHCP' | 'dualRhcpLhcp' | 'linearHorizontal' | 'linearVertical' (Required): polarization. eg (RHCP, LHCP)

## ContactProfileLinkChannel
### Properties
* **bandwidthMHz**: int (Required): Bandwidth in MHz
* **centerFrequencyMHz**: int (Required): Center Frequency in MHz
* **decodingConfiguration**: string: Configuration for decoding
* **demodulationConfiguration**: string: Configuration for demodulation
* **encodingConfiguration**: string: Configuration for encoding
* **endPoint**: [EndPoint](#endpoint) (Required): Customer End point to store/retrieve data during a contact.
* **modulationConfiguration**: string: Configuration for modulation

## EndPoint
### Properties
* **endPointName**: string (Required): Name of an end point.
* **ipAddress**: string (Required): IP Address.
* **port**: string (Required): TCP port to listen on to receive data.
* **protocol**: 'TCP' | 'UDP' (Required): Protocol either UDP or TCP.

## SystemData
### Properties
* **createdAt**: string: The timestamp of resource creation (UTC).
* **createdBy**: string: The identity that created the resource.
* **createdByType**: 'Application' | 'Key' | 'ManagedIdentity' | 'User': The type of identity that created the resource.
* **lastModifiedAt**: string: The timestamp of resource last modification (UTC)
* **lastModifiedBy**: string: The identity that last modified the resource.
* **lastModifiedByType**: 'Application' | 'Key' | 'ManagedIdentity' | 'User': The type of identity that created the resource.

## TrackedResourceTags
### Properties
### Additional Properties
* **Additional Properties Type**: string

## SpacecraftsProperties
### Properties
* **authorizationStatus**: 'Allowed' | 'Denied' | 'Pending' (ReadOnly): Authorization status of spacecraft.
* **authorizationStatusExtended**: string (ReadOnly): Details of the authorization status.
* **links**: [SpacecraftLink](#spacecraftlink)[]: Links of the Spacecraft
* **noradId**: string (Required): NORAD ID of the spacecraft.
* **titleLine**: string: Title line of Two Line Element (TLE).
* **tleLine1**: string: Line 1 of Two Line Element (TLE).
* **tleLine2**: string: Line 2 of Two Line Element (TLE).

## SpacecraftLink
### Properties
* **bandwidthMHz**: int (Required): Bandwidth in MHz
* **centerFrequencyMHz**: int (Required): Center Frequency in MHz
* **direction**: 'downlink' | 'uplink' (Required): Direction (uplink or downlink)
* **polarization**: 'LHCP' | 'RHCP' | 'dualRhcpLhcp' | 'linearHorizontal' | 'linearVertical' (Required): polarization. eg (RHCP, LHCP)

## TrackedResourceTags
### Properties
### Additional Properties
* **Additional Properties Type**: string

## ContactsProperties
### Properties
* **contactProfile**: [ResourceReference](#resourcereference) (Required): Resource Reference
* **endAzimuthDegrees**: int (ReadOnly): Azimuth of the antenna at the end of the contact in decimal degrees.
* **endElevationDegrees**: int (ReadOnly): Spacecraft elevation above the horizon at contact end.
* **errorMessage**: string (ReadOnly): Any error message while scheduling a contact.
* **groundStationName**: string (Required): Azure Ground Station name.
* **maximumElevationDegrees**: int (ReadOnly): Maximum elevation of the antenna during the contact in decimal degrees.
* **reservationEndTime**: string (Required): Reservation end time of a contact.
* **reservationStartTime**: string (Required): Reservation start time of a contact.
* **rxEndTime**: string (ReadOnly): Receive end time of a contact.
* **rxStartTime**: string (ReadOnly): Receive start time of a contact.
* **startAzimuthDegrees**: int (ReadOnly): Azimuth of the antenna at the start of the contact in decimal degrees.
* **startElevationDegrees**: int (ReadOnly): Spacecraft elevation above the horizon at contact start.
* **status**: 'cancelled' | 'failed' | 'providerCancelled' | 'scheduled' | 'succeeded' (ReadOnly): Status of a contact.
* **txEndTime**: string (ReadOnly): Transmit end time of a contact.
* **txStartTime**: string (ReadOnly): Transmit start time of a contact.

## ResourceReference
### Properties
* **id**: string: Resource ID.

## ContactParameters
### Properties
* **contactProfile**: [ResourceReference](#resourcereference) (Required, WriteOnly): Resource Reference
* **endTime**: string (Required, WriteOnly): End time of a contact.
* **groundStationName**: string (Required, WriteOnly): Name of Azure Ground Station.
* **startTime**: string (Required, WriteOnly): Start time of a contact.

## AvailableContactsListResult
### Properties
* **nextLink**: string (ReadOnly): The URL to get the next set of results.
* **value**: [AvailableContacts](#availablecontacts)[] (ReadOnly): A list of available contacts

## AvailableContacts
### Properties
* **groundStationName**: string (ReadOnly): Name of Azure Ground Station.
* **properties**: [ContactInstanceProperties](#contactinstanceproperties) (ReadOnly): Contact Instance Properties
* **spacecraft**: [ResourceReference](#resourcereference) (ReadOnly): Resource Reference

## ContactInstanceProperties
### Properties
* **endAzimuthDegrees**: int (ReadOnly): Azimuth of the antenna at the end of the contact in decimal degrees.
* **endElevationDegrees**: int (ReadOnly): Spacecraft elevation above the horizon at contact end.
* **maximumElevationDegrees**: int (ReadOnly): Maximum elevation of the antenna during the contact in decimal degrees.
* **rxEndTime**: string (ReadOnly): Time to lost receiving a signal.
* **rxStartTime**: string (ReadOnly): Earliest time to receive a signal.
* **startAzimuthDegrees**: int (ReadOnly): Azimuth of the antenna at the start of the contact in decimal degrees.
* **startElevationDegrees**: int (ReadOnly): Spacecraft elevation above the horizon at contact start.
* **txEndTime**: string (ReadOnly): Time at which antenna transmit will be disabled.
* **txStartTime**: string (ReadOnly): Time at which antenna transmit will be enabled.

