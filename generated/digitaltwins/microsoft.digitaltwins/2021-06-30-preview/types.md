# Microsoft.DigitalTwins @ 2021-06-30-preview

## Resource Microsoft.DigitalTwins/digitalTwinsInstances@2021-06-30-preview
* **Valid Scope(s)**: ResourceGroup
### Properties
* **apiVersion**: '2021-06-30-preview' (ReadOnly, DeployTimeConstant): The resource api version
* **id**: string (ReadOnly, DeployTimeConstant): The resource id
* **identity**: [DigitalTwinsIdentity](#digitaltwinsidentity): The managed identity for the DigitalTwinsInstance.
* **location**: string (Required): The resource location.
* **name**: string (Required, DeployTimeConstant): The resource name
* **properties**: [DigitalTwinsProperties](#digitaltwinsproperties): The properties of a DigitalTwinsInstance.
* **systemData**: [SystemData](#systemdata) (ReadOnly): Metadata pertaining to creation and last modification of the resource.
* **tags**: [DigitalTwinsResourceTags](#digitaltwinsresourcetags): The resource tags.
* **type**: 'Microsoft.DigitalTwins/digitalTwinsInstances' (ReadOnly, DeployTimeConstant): The resource type

## Resource Microsoft.DigitalTwins/digitalTwinsInstances/endpoints@2021-06-30-preview
* **Valid Scope(s)**: ResourceGroup
### Properties
* **apiVersion**: '2021-06-30-preview' (ReadOnly, DeployTimeConstant): The resource api version
* **id**: string (ReadOnly, DeployTimeConstant): The resource id
* **name**: string (Required, DeployTimeConstant): The resource name
* **properties**: [DigitalTwinsEndpointResourceProperties](#digitaltwinsendpointresourceproperties) (Required): Properties related to Digital Twins Endpoint
* **systemData**: [SystemData](#systemdata) (ReadOnly): Metadata pertaining to creation and last modification of the resource.
* **type**: 'Microsoft.DigitalTwins/digitalTwinsInstances/endpoints' (ReadOnly, DeployTimeConstant): The resource type

## Resource Microsoft.DigitalTwins/digitalTwinsInstances/privateEndpointConnections@2021-06-30-preview
* **Valid Scope(s)**: ResourceGroup
### Properties
* **apiVersion**: '2021-06-30-preview' (ReadOnly, DeployTimeConstant): The resource api version
* **id**: string (ReadOnly, DeployTimeConstant): The resource id
* **name**: string (Required, DeployTimeConstant): The resource name
* **properties**: [ConnectionProperties](#connectionproperties) (Required): The properties of a private endpoint connection.
* **systemData**: [SystemData](#systemdata) (ReadOnly): Metadata pertaining to creation and last modification of the resource.
* **type**: 'Microsoft.DigitalTwins/digitalTwinsInstances/privateEndpointConnections' (ReadOnly, DeployTimeConstant): The resource type

## Resource Microsoft.DigitalTwins/digitalTwinsInstances/timeSeriesDatabaseConnections@2021-06-30-preview
* **Valid Scope(s)**: ResourceGroup
### Properties
* **apiVersion**: '2021-06-30-preview' (ReadOnly, DeployTimeConstant): The resource api version
* **id**: string (ReadOnly, DeployTimeConstant): The resource id
* **name**: string (Required, DeployTimeConstant): The resource name
* **properties**: [TimeSeriesDatabaseConnectionProperties](#timeseriesdatabaseconnectionproperties): Properties of a time series database connection resource.
* **systemData**: [SystemData](#systemdata) (ReadOnly): Metadata pertaining to creation and last modification of the resource.
* **type**: 'Microsoft.DigitalTwins/digitalTwinsInstances/timeSeriesDatabaseConnections' (ReadOnly, DeployTimeConstant): The resource type

## DigitalTwinsIdentity
### Properties
* **principalId**: string (ReadOnly): The object id of the Managed Identity Resource. This will be sent to the RP from ARM via the x-ms-identity-principal-id header in the PUT request if the resource has a systemAssigned(implicit) identity
* **tenantId**: string (ReadOnly): The tenant id of the Managed Identity Resource. This will be sent to the RP from ARM via the x-ms-client-tenant-id header in the PUT request if the resource has a systemAssigned(implicit) identity
* **type**: 'None' | 'SystemAssigned': The type of Managed Identity used by the DigitalTwinsInstance. Only SystemAssigned is supported.

## DigitalTwinsProperties
### Properties
* **createdTime**: string (ReadOnly): Time when DigitalTwinsInstance was created.
* **hostName**: string (ReadOnly): Api endpoint to work with DigitalTwinsInstance.
* **lastUpdatedTime**: string (ReadOnly): Time when DigitalTwinsInstance was updated.
* **privateEndpointConnections**: [PrivateEndpointConnection](#privateendpointconnection)[]: The private endpoint connections.
* **provisioningState**: 'Canceled' | 'Deleted' | 'Deleting' | 'Failed' | 'Moving' | 'Provisioning' | 'Restoring' | 'Succeeded' | 'Suspending' | 'Updating' | 'Warning' (ReadOnly): The provisioning state.
* **publicNetworkAccess**: 'Disabled' | 'Enabled': Public network access for the DigitalTwinsInstance.

## PrivateEndpointConnection
### Properties
* **id**: string (ReadOnly): The resource identifier.
* **name**: string (ReadOnly): The resource name.
* **properties**: [ConnectionProperties](#connectionproperties) (Required): The properties of a private endpoint connection.
* **systemData**: [SystemData](#systemdata) (ReadOnly): Metadata pertaining to creation and last modification of the resource.
* **type**: string (ReadOnly): The resource type.

## ConnectionProperties
### Properties
* **groupIds**: string[]: The list of group ids for the private endpoint connection.
* **privateEndpoint**: [PrivateEndpoint](#privateendpoint): The private endpoint property of a private endpoint connection.
* **privateLinkServiceConnectionState**: [ConnectionPropertiesPrivateLinkServiceConnectionState](#connectionpropertiesprivatelinkserviceconnectionstate): The connection state.
* **provisioningState**: 'Approved' | 'Disconnected' | 'Pending' | 'Rejected' (ReadOnly): The provisioning state.

## PrivateEndpoint
### Properties
* **id**: string (ReadOnly): The resource identifier.

## ConnectionPropertiesPrivateLinkServiceConnectionState
### Properties
* **actionsRequired**: string: Actions required for a private endpoint connection.
* **description**: string (Required): The description for the current state of a private endpoint connection.
* **status**: 'Approved' | 'Disconnected' | 'Pending' | 'Rejected' (Required): The status of a private endpoint connection.

## SystemData
### Properties
* **createdAt**: string: The timestamp of resource creation (UTC).
* **createdBy**: string: The identity that created the resource.
* **createdByType**: 'Application' | 'Key' | 'ManagedIdentity' | 'User': The type of identity that created the resource.
* **lastModifiedAt**: string: The timestamp of resource last modification (UTC)
* **lastModifiedBy**: string: The identity that last modified the resource.
* **lastModifiedByType**: 'Application' | 'Key' | 'ManagedIdentity' | 'User': The type of identity that created the resource.

## DigitalTwinsResourceTags
### Properties
### Additional Properties
* **Additional Properties Type**: string

## DigitalTwinsEndpointResourceProperties
* **Discriminator**: endpointType

### Base Properties
* **authenticationType**: 'IdentityBased' | 'KeyBased': Specifies the authentication type being used for connecting to the endpoint. Defaults to 'KeyBased'. If 'KeyBased' is selected, a connection string must be specified (at least the primary connection string). If 'IdentityBased' is select, the endpointUri and entityPath properties must be specified.
* **createdTime**: string (ReadOnly): Time when the Endpoint was added to DigitalTwinsInstance.
* **deadLetterSecret**: string: Dead letter storage secret for key-based authentication. Will be obfuscated during read.
* **deadLetterUri**: string: Dead letter storage URL for identity-based authentication.
* **provisioningState**: 'Canceled' | 'Deleted' | 'Deleting' | 'Disabled' | 'Failed' | 'Moving' | 'Provisioning' | 'Restoring' | 'Succeeded' | 'Suspending' | 'Warning' (ReadOnly): The provisioning state.
### EventGrid
#### Properties
* **accessKey1**: string (Required): EventGrid secondary accesskey. Will be obfuscated during read.
* **accessKey2**: string: EventGrid secondary accesskey. Will be obfuscated during read.
* **endpointType**: 'EventGrid' (Required): The type of Digital Twins endpoint
* **TopicEndpoint**: string (Required): EventGrid Topic Endpoint.

### EventHub
#### Properties
* **connectionStringPrimaryKey**: string: PrimaryConnectionString of the endpoint for key-based authentication. Will be obfuscated during read.
* **connectionStringSecondaryKey**: string: SecondaryConnectionString of the endpoint for key-based authentication. Will be obfuscated during read.
* **endpointType**: 'EventHub' (Required): The type of Digital Twins endpoint
* **endpointUri**: string: The URL of the EventHub namespace for identity-based authentication. It must include the protocol 'sb://'.
* **entityPath**: string: The EventHub name in the EventHub namespace for identity-based authentication.

### ServiceBus
#### Properties
* **endpointType**: 'ServiceBus' (Required): The type of Digital Twins endpoint
* **endpointUri**: string: The URL of the ServiceBus namespace for identity-based authentication. It must include the protocol 'sb://'.
* **entityPath**: string: The ServiceBus Topic name for identity-based authentication.
* **primaryConnectionString**: string: PrimaryConnectionString of the endpoint for key-based authentication. Will be obfuscated during read.
* **secondaryConnectionString**: string: SecondaryConnectionString of the endpoint for key-based authentication. Will be obfuscated during read.


## TimeSeriesDatabaseConnectionProperties
* **Discriminator**: connectionType

### Base Properties
* **provisioningState**: 'Canceled' | 'Deleted' | 'Deleting' | 'Disabled' | 'Failed' | 'Moving' | 'Provisioning' | 'Restoring' | 'Succeeded' | 'Suspending' | 'Warning' (ReadOnly): The provisioning state.
### AzureDataExplorerConnectionProperties
#### Properties
* **adxDatabaseName**: string (Required): The name of the Azure Data Explorer database.
* **adxEndpointUri**: string (Required): The URI of the Azure Data Explorer endpoint.
* **adxResourceId**: string (Required): The resource ID of the Azure Data Explorer cluster.
* **adxTableName**: string: The name of the Azure Data Explorer table.
* **connectionType**: 'AzureDataExplorer' (Required): The type of time series connection resource.
* **eventHubConsumerGroup**: string: The EventHub consumer group to use when ADX reads from EventHub. Defaults to $Default.
* **eventHubEndpointUri**: string (Required): The URL of the EventHub namespace for identity-based authentication. It must include the protocol sb://
* **eventHubEntityPath**: string (Required): The EventHub name in the EventHub namespace for identity-based authentication.
* **eventHubNamespaceResourceId**: string (Required): The resource ID of the EventHub namespace.


