# Microsoft.Kusto @ 2019-01-21

## Resource Microsoft.Kusto/clusters@2019-01-21
* **Valid Scope(s)**: ResourceGroup
### Properties
* **apiVersion**: '2019-01-21' (ReadOnly, DeployTimeConstant): The resource api version
* **id**: string (ReadOnly, DeployTimeConstant): The resource id
* **location**: string (Required): The geo-location where the resource lives
* **name**: string (Required, DeployTimeConstant): The resource name
* **properties**: [ClusterProperties](#clusterproperties): Class representing the Kusto cluster properties.
* **sku**: [AzureSku](#azuresku) (Required): Azure SKU definition.
* **tags**: [TrackedResourceTags](#trackedresourcetags): Resource tags.
* **type**: 'Microsoft.Kusto/clusters' (ReadOnly, DeployTimeConstant): The resource type

## Resource Microsoft.Kusto/clusters/databases@2019-01-21
* **Valid Scope(s)**: ResourceGroup
### Properties
* **apiVersion**: '2019-01-21' (ReadOnly, DeployTimeConstant): The resource api version
* **id**: string (ReadOnly, DeployTimeConstant): The resource id
* **location**: string: Resource location.
* **name**: string (Required, DeployTimeConstant): The resource name
* **properties**: [DatabaseProperties](#databaseproperties): Class representing the Kusto database properties.
* **type**: 'Microsoft.Kusto/clusters/databases' (ReadOnly, DeployTimeConstant): The resource type

## Resource Microsoft.Kusto/clusters/databases/dataConnections@2019-01-21
* **Valid Scope(s)**: ResourceGroup
* **Discriminator**: kind

### Base Properties
* **apiVersion**: '2019-01-21' (ReadOnly, DeployTimeConstant): The resource api version
* **id**: string (ReadOnly, DeployTimeConstant): The resource id
* **location**: string: Resource location.
* **name**: string (Required, DeployTimeConstant): The resource name
* **type**: 'Microsoft.Kusto/clusters/databases/dataConnections' (ReadOnly, DeployTimeConstant): The resource type
### EventGridDataConnection
#### Properties
* **kind**: 'EventGrid' (Required): Kind of the endpoint for the data connection
* **properties**: [EventGridConnectionProperties](#eventgridconnectionproperties): Class representing the Kusto event grid connection properties.

### EventHubDataConnection
#### Properties
* **kind**: 'EventHub' (Required): Kind of the endpoint for the data connection
* **properties**: [EventHubConnectionProperties](#eventhubconnectionproperties): Class representing the Kusto event hub connection properties.


## Function listPrincipals (Microsoft.Kusto/clusters/databases@2019-01-21)
* **Resource**: Microsoft.Kusto/clusters/databases
* **ApiVersion**: 2019-01-21
* **Output**: [DatabasePrincipalListResult](#databaseprincipallistresult)

## ClusterProperties
### Properties
* **dataIngestionUri**: string (ReadOnly): The cluster data ingestion URI.
* **provisioningState**: 'Creating' | 'Deleting' | 'Failed' | 'Running' | 'Succeeded' (ReadOnly): The provisioned state of the resource.
* **state**: 'Creating' | 'Deleted' | 'Deleting' | 'Running' | 'Starting' | 'Stopped' | 'Stopping' | 'Unavailable' | 'Updating' (ReadOnly): The state of the resource.
* **trustedExternalTenants**: [TrustedExternalTenant](#trustedexternaltenant)[]: The cluster's external tenants.
* **uri**: string (ReadOnly): The cluster URI.

## TrustedExternalTenant
### Properties
* **value**: string: GUID representing an external tenant.

## AzureSku
### Properties
* **capacity**: int: The number of instances of the cluster.
* **name**: 'Dev(No SLA)_Standard_D11_v2' | 'Standard_D11_v2' | 'Standard_D12_v2' | 'Standard_D13_v2' | 'Standard_D14_v2' | 'Standard_DS13_v2+1TB_PS' | 'Standard_DS13_v2+2TB_PS' | 'Standard_DS14_v2+3TB_PS' | 'Standard_DS14_v2+4TB_PS' | 'Standard_L16s' | 'Standard_L4s' | 'Standard_L8s' (Required): SKU name.
* **tier**: 'Basic' | 'Standard' (Required): SKU tier.

## TrackedResourceTags
### Properties
### Additional Properties
* **Additional Properties Type**: string

## DatabaseProperties
### Properties
* **hotCachePeriod**: string: The time the data that should be kept in cache for fast queries in TimeSpan.
* **provisioningState**: 'Creating' | 'Deleting' | 'Failed' | 'Running' | 'Succeeded' (ReadOnly): The provisioned state of the resource.
* **softDeletePeriod**: string: The time the data should be kept before it stops being accessible to queries in TimeSpan.
* **statistics**: [DatabaseStatistics](#databasestatistics) (ReadOnly): A class that contains database statistics information.

## DatabaseStatistics
### Properties
* **size**: int: The database size - the total size of compressed data and index in bytes.

## EventGridConnectionProperties
### Properties
* **consumerGroup**: string (Required): The event hub consumer group.
* **dataFormat**: 'AVRO' | 'CSV' | 'JSON' | 'MULTIJSON' | 'PSV' | 'RAW' | 'SCSV' | 'SINGLEJSON' | 'SOHSV' | 'TSV' | 'TXT' (Required): The data format of the message. Optionally the data format can be added to each message.
* **eventHubResourceId**: string (Required): The resource ID where the event grid is configured to send events.
* **mappingRuleName**: string: The mapping rule to be used to ingest the data. Optionally the mapping information can be added to each message.
* **storageAccountResourceId**: string (Required): The resource ID of the storage account where the data resides.
* **tableName**: string (Required): The table where the data should be ingested. Optionally the table information can be added to each message.

## EventHubConnectionProperties
### Properties
* **consumerGroup**: string (Required): The event hub consumer group.
* **dataFormat**: 'AVRO' | 'CSV' | 'JSON' | 'MULTIJSON' | 'PSV' | 'RAW' | 'SCSV' | 'SINGLEJSON' | 'SOHSV' | 'TSV' | 'TXT': The data format of the message. Optionally the data format can be added to each message.
* **eventHubResourceId**: string (Required): The resource ID of the event hub to be used to create a data connection.
* **mappingRuleName**: string: The mapping rule to be used to ingest the data. Optionally the mapping information can be added to each message.
* **tableName**: string: The table where the data should be ingested. Optionally the table information can be added to each message.

## DatabasePrincipalListResult
### Properties
* **value**: [DatabasePrincipal](#databaseprincipal)[] (ReadOnly): The list of Kusto database principals.

## DatabasePrincipal
### Properties
* **appId**: string (ReadOnly): Application id - relevant only for application principal type.
* **email**: string (ReadOnly): Database principal email if exists.
* **fqn**: string (ReadOnly): Database principal fully qualified name.
* **name**: string (ReadOnly): Database principal name.
* **role**: 'Admin' | 'Ingestor' | 'Monitor' | 'UnrestrictedViewers' | 'User' | 'Viewer' (ReadOnly): Database principal role.
* **type**: 'App' | 'Group' | 'User' (ReadOnly): Database principal type.

