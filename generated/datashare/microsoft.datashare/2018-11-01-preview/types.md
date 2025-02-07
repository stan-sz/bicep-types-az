# Microsoft.DataShare @ 2018-11-01-preview

## Resource Microsoft.DataShare/accounts@2018-11-01-preview
* **Valid Scope(s)**: ResourceGroup
### Properties
* **apiVersion**: '2018-11-01-preview' (ReadOnly, DeployTimeConstant): The resource api version
* **id**: string (ReadOnly, DeployTimeConstant): The resource id
* **identity**: [Identity](#identity) (Required): Identity of resource
* **location**: string: Location of the azure resource.
* **name**: string (Required, DeployTimeConstant): The resource name
* **properties**: [AccountProperties](#accountproperties): Account property bag.
* **tags**: [DefaultDtoTags](#defaultdtotags): Tags on the azure resource.
* **type**: 'Microsoft.DataShare/accounts' (ReadOnly, DeployTimeConstant): The resource type

## Resource Microsoft.DataShare/accounts/shares@2018-11-01-preview
* **Valid Scope(s)**: ResourceGroup
### Properties
* **apiVersion**: '2018-11-01-preview' (ReadOnly, DeployTimeConstant): The resource api version
* **id**: string (ReadOnly, DeployTimeConstant): The resource id
* **name**: string (Required, DeployTimeConstant): The resource name
* **properties**: [ShareProperties](#shareproperties): Share property bag.
* **type**: 'Microsoft.DataShare/accounts/shares' (ReadOnly, DeployTimeConstant): The resource type

## Resource Microsoft.DataShare/accounts/shares/dataSets@2018-11-01-preview
* **Valid Scope(s)**: ResourceGroup
* **Discriminator**: kind

### Base Properties
* **apiVersion**: '2018-11-01-preview' (ReadOnly, DeployTimeConstant): The resource api version
* **id**: string (ReadOnly, DeployTimeConstant): The resource id
* **name**: string (Required, DeployTimeConstant): The resource name
* **type**: 'Microsoft.DataShare/accounts/shares/dataSets' (ReadOnly, DeployTimeConstant): The resource type
### AdlsGen1FileDataSet
#### Properties
* **kind**: 'AdlsGen1File' (Required): Kind of data set.
* **properties**: [AdlsGen1FileProperties](#adlsgen1fileproperties) (Required): Properties of the ADLS Gen1 file data set.

### AdlsGen1FolderDataSet
#### Properties
* **kind**: 'AdlsGen1Folder' (Required): Kind of data set.
* **properties**: [AdlsGen1FolderProperties](#adlsgen1folderproperties) (Required): Properties of the ADLS Gen1 folder data set.

### AdlsGen2FileDataSet
#### Properties
* **kind**: 'AdlsGen2File' (Required): Kind of data set.
* **properties**: [AdlsGen2FileProperties](#adlsgen2fileproperties) (Required): Properties of the ADLS Gen2 file data set.

### AdlsGen2FileSystemDataSet
#### Properties
* **kind**: 'AdlsGen2FileSystem' (Required): Kind of data set.
* **properties**: [AdlsGen2FileSystemProperties](#adlsgen2filesystemproperties) (Required): Properties of the ADLS Gen2 file system data set.

### AdlsGen2FolderDataSet
#### Properties
* **kind**: 'AdlsGen2Folder' (Required): Kind of data set.
* **properties**: [AdlsGen2FolderProperties](#adlsgen2folderproperties) (Required): Properties of the ADLS Gen2 folder data set.

### BlobDataSet
#### Properties
* **kind**: 'Blob' (Required): Kind of data set.
* **properties**: [BlobProperties](#blobproperties) (Required): Properties of the blob data set.

### BlobFolderDataSet
#### Properties
* **kind**: 'BlobFolder' (Required): Kind of data set.
* **properties**: [BlobFolderProperties](#blobfolderproperties) (Required): Properties of the blob folder data set.

### BlobContainerDataSet
#### Properties
* **kind**: 'Container' (Required): Kind of data set.
* **properties**: [BlobContainerProperties](#blobcontainerproperties) (Required): Properties of the BLOB container data set.

### KustoClusterDataSet
#### Properties
* **kind**: 'KustoCluster' (Required): Kind of data set.
* **properties**: [KustoClusterDataSetProperties](#kustoclusterdatasetproperties) (Required): Properties of the kusto cluster data set.

### KustoDatabaseDataSet
#### Properties
* **kind**: 'KustoDatabase' (Required): Kind of data set.
* **properties**: [KustoDatabaseDataSetProperties](#kustodatabasedatasetproperties) (Required): Properties of the kusto database data set.

### SqlDBTableDataSet
#### Properties
* **kind**: 'SqlDBTable' (Required): Kind of data set.
* **properties**: [SqlDBTableProperties](#sqldbtableproperties): Properties of the SQL DB table data set.

### SqlDWTableDataSet
#### Properties
* **kind**: 'SqlDWTable' (Required): Kind of data set.
* **properties**: [SqlDWTableProperties](#sqldwtableproperties): Properties of the SQL DW table data set.


## Resource Microsoft.DataShare/accounts/shares/invitations@2018-11-01-preview
* **Valid Scope(s)**: ResourceGroup
### Properties
* **apiVersion**: '2018-11-01-preview' (ReadOnly, DeployTimeConstant): The resource api version
* **id**: string (ReadOnly, DeployTimeConstant): The resource id
* **name**: string (Required, DeployTimeConstant): The resource name
* **properties**: [InvitationProperties](#invitationproperties): Invitation property bag.
* **type**: 'Microsoft.DataShare/accounts/shares/invitations' (ReadOnly, DeployTimeConstant): The resource type

## Resource Microsoft.DataShare/accounts/shares/synchronizationSettings@2018-11-01-preview
* **Valid Scope(s)**: ResourceGroup
* **Discriminator**: kind

### Base Properties
* **apiVersion**: '2018-11-01-preview' (ReadOnly, DeployTimeConstant): The resource api version
* **id**: string (ReadOnly, DeployTimeConstant): The resource id
* **name**: string (Required, DeployTimeConstant): The resource name
* **type**: 'Microsoft.DataShare/accounts/shares/synchronizationSettings' (ReadOnly, DeployTimeConstant): The resource type
### ScheduledSynchronizationSetting
#### Properties
* **kind**: 'ScheduleBased' (Required): Kind of synchronization setting.
* **properties**: [ScheduledSynchronizationSettingProperties](#scheduledsynchronizationsettingproperties) (Required): A Scheduled synchronization setting data transfer object.


## Resource Microsoft.DataShare/accounts/shareSubscriptions@2018-11-01-preview
* **Valid Scope(s)**: ResourceGroup
### Properties
* **apiVersion**: '2018-11-01-preview' (ReadOnly, DeployTimeConstant): The resource api version
* **id**: string (ReadOnly, DeployTimeConstant): The resource id
* **name**: string (Required, DeployTimeConstant): The resource name
* **properties**: [ShareSubscriptionProperties](#sharesubscriptionproperties) (Required): Share subscription property bag.
* **type**: 'Microsoft.DataShare/accounts/shareSubscriptions' (ReadOnly, DeployTimeConstant): The resource type

## Resource Microsoft.DataShare/accounts/shareSubscriptions/dataSetMappings@2018-11-01-preview
* **Valid Scope(s)**: ResourceGroup
* **Discriminator**: kind

### Base Properties
* **apiVersion**: '2018-11-01-preview' (ReadOnly, DeployTimeConstant): The resource api version
* **id**: string (ReadOnly, DeployTimeConstant): The resource id
* **name**: string (Required, DeployTimeConstant): The resource name
* **type**: 'Microsoft.DataShare/accounts/shareSubscriptions/dataSetMappings' (ReadOnly, DeployTimeConstant): The resource type
### AdlsGen2FileDataSetMapping
#### Properties
* **kind**: 'AdlsGen2File' (Required): Kind of data set mapping.
* **properties**: [AdlsGen2FileDataSetMappingProperties](#adlsgen2filedatasetmappingproperties) (Required): ADLS Gen 2 file data set mapping property bag.

### AdlsGen2FileSystemDataSetMapping
#### Properties
* **kind**: 'AdlsGen2FileSystem' (Required): Kind of data set mapping.
* **properties**: [AdlsGen2FileSystemDataSetMappingProperties](#adlsgen2filesystemdatasetmappingproperties) (Required): ADLS Gen 2 file system data set mapping property bag.

### AdlsGen2FolderDataSetMapping
#### Properties
* **kind**: 'AdlsGen2Folder' (Required): Kind of data set mapping.
* **properties**: [AdlsGen2FolderDataSetMappingProperties](#adlsgen2folderdatasetmappingproperties) (Required): ADLS Gen 2 folder data set mapping property bag.

### BlobDataSetMapping
#### Properties
* **kind**: 'Blob' (Required): Kind of data set mapping.
* **properties**: [BlobMappingProperties](#blobmappingproperties) (Required): Azure storage Blob data set mapping property bag.

### BlobFolderDataSetMapping
#### Properties
* **kind**: 'BlobFolder' (Required): Kind of data set mapping.
* **properties**: [BlobFolderMappingProperties](#blobfoldermappingproperties) (Required): Azure storage Blob folder data set mapping property bag.

### BlobContainerDataSetMapping
#### Properties
* **kind**: 'Container' (Required): Kind of data set mapping.
* **properties**: [BlobContainerMappingProperties](#blobcontainermappingproperties) (Required): Azure storage Blob container data set mapping property bag.

### KustoClusterDataSetMapping
#### Properties
* **kind**: 'KustoCluster' (Required): Kind of data set mapping.
* **properties**: [KustoClusterDataSetMappingProperties](#kustoclusterdatasetmappingproperties) (Required): Properties of the Kusto cluster data set mapping

### KustoDatabaseDataSetMapping
#### Properties
* **kind**: 'KustoDatabase' (Required): Kind of data set mapping.
* **properties**: [KustoDatabaseDataSetMappingProperties](#kustodatabasedatasetmappingproperties) (Required): Properties of the Kusto database data set mapping

### SqlDBTableDataSetMapping
#### Properties
* **kind**: 'SqlDBTable' (Required): Kind of data set mapping.
* **properties**: [SqlDBTableDataSetMappingProperties](#sqldbtabledatasetmappingproperties) (Required): Properties of the SQL DB table data set mapping.

### SqlDWTableDataSetMapping
#### Properties
* **kind**: 'SqlDWTable' (Required): Kind of data set mapping.
* **properties**: [SqlDWTableDataSetMappingProperties](#sqldwtabledatasetmappingproperties) (Required): Properties of the SQL DW table data set mapping.


## Resource Microsoft.DataShare/accounts/shareSubscriptions/triggers@2018-11-01-preview
* **Valid Scope(s)**: ResourceGroup
* **Discriminator**: kind

### Base Properties
* **apiVersion**: '2018-11-01-preview' (ReadOnly, DeployTimeConstant): The resource api version
* **id**: string (ReadOnly, DeployTimeConstant): The resource id
* **name**: string (Required, DeployTimeConstant): The resource name
* **type**: 'Microsoft.DataShare/accounts/shareSubscriptions/triggers' (ReadOnly, DeployTimeConstant): The resource type
### ScheduledTrigger
#### Properties
* **kind**: 'ScheduleBased' (Required): Kind of synchronization on trigger.
* **properties**: [ScheduledTriggerProperties](#scheduledtriggerproperties) (Required): A Scheduled trigger data transfer object.


## Function listSourceShareSynchronizationSettings (Microsoft.DataShare/accounts/shareSubscriptions@2018-11-01-preview)
* **Resource**: Microsoft.DataShare/accounts/shareSubscriptions
* **ApiVersion**: 2018-11-01-preview
* **Output**: [SourceShareSynchronizationSettingList](#sourcesharesynchronizationsettinglist)

## Function listSynchronizationDetails (Microsoft.DataShare/accounts/shares@2018-11-01-preview)
* **Resource**: Microsoft.DataShare/accounts/shares
* **ApiVersion**: 2018-11-01-preview
* **Input**: [ShareSynchronization](#sharesynchronization)
* **Output**: [SynchronizationDetailsList](#synchronizationdetailslist)

## Function listSynchronizationDetails (Microsoft.DataShare/accounts/shareSubscriptions@2018-11-01-preview)
* **Resource**: Microsoft.DataShare/accounts/shareSubscriptions
* **ApiVersion**: 2018-11-01-preview
* **Input**: [ShareSubscriptionSynchronization](#sharesubscriptionsynchronization)
* **Output**: [SynchronizationDetailsList](#synchronizationdetailslist)

## Function listSynchronizations (Microsoft.DataShare/accounts/shares@2018-11-01-preview)
* **Resource**: Microsoft.DataShare/accounts/shares
* **ApiVersion**: 2018-11-01-preview
* **Output**: [ShareSynchronizationList](#sharesynchronizationlist)

## Function listSynchronizations (Microsoft.DataShare/accounts/shareSubscriptions@2018-11-01-preview)
* **Resource**: Microsoft.DataShare/accounts/shareSubscriptions
* **ApiVersion**: 2018-11-01-preview
* **Output**: [ShareSubscriptionSynchronizationList](#sharesubscriptionsynchronizationlist)

## Identity
### Properties
* **principalId**: string (ReadOnly): service principal Id
* **tenantId**: string (ReadOnly): Tenant Id
* **type**: 'SystemAssigned': Identity Type

## AccountProperties
### Properties
* **createdAt**: string (ReadOnly): Time at which the account was created.
* **provisioningState**: 'Creating' | 'Deleting' | 'Failed' | 'Moving' | 'Succeeded' (ReadOnly): Provisioning state of the Account
* **userEmail**: string (ReadOnly): Email of the user who created the resource
* **userName**: string (ReadOnly): Name of the user who created the resource

## DefaultDtoTags
### Properties
### Additional Properties
* **Additional Properties Type**: string

## ShareProperties
### Properties
* **createdAt**: string (ReadOnly): Time at which the share was created.
* **description**: string: Share description.
* **provisioningState**: 'Creating' | 'Deleting' | 'Failed' | 'Moving' | 'Succeeded' (ReadOnly): Provisioning state of the Account
* **shareKind**: 'CopyBased' | 'InPlace': Share kind.
* **terms**: string: Share terms.
* **userEmail**: string (ReadOnly): Email of the user who created the resource
* **userName**: string (ReadOnly): Name of the user who created the resource

## AdlsGen1FileProperties
### Properties
* **accountName**: string (Required): The ADLS account name.
* **dataSetId**: string (ReadOnly): Unique id for identifying a data set resource
* **fileName**: string (Required): The file name in the ADLS account.
* **folderPath**: string (Required): The folder path within the ADLS account.
* **resourceGroup**: string (Required): Resource group of ADLS account.
* **subscriptionId**: string (Required): Subscription id of ADLS account.

## AdlsGen1FolderProperties
### Properties
* **accountName**: string (Required): The ADLS account name.
* **dataSetId**: string (ReadOnly): Unique id for identifying a data set resource
* **folderPath**: string (Required): The folder path within the ADLS account.
* **resourceGroup**: string (Required): Resource group of ADLS account.
* **subscriptionId**: string (Required): Subscription id of ADLS account.

## AdlsGen2FileProperties
### Properties
* **dataSetId**: string (ReadOnly): Unique id for identifying a data set resource
* **filePath**: string (Required): File path within the file system.
* **fileSystem**: string (Required): File system to which the file belongs.
* **resourceGroup**: string (Required): Resource group of storage account
* **storageAccountName**: string (Required): Storage account name of the source data set
* **subscriptionId**: string (Required): Subscription id of storage account

## AdlsGen2FileSystemProperties
### Properties
* **dataSetId**: string (ReadOnly): Unique id for identifying a data set resource
* **fileSystem**: string (Required): The file system name.
* **resourceGroup**: string (Required): Resource group of storage account
* **storageAccountName**: string (Required): Storage account name of the source data set
* **subscriptionId**: string (Required): Subscription id of storage account

## AdlsGen2FolderProperties
### Properties
* **dataSetId**: string (ReadOnly): Unique id for identifying a data set resource
* **fileSystem**: string (Required): File system to which the folder belongs.
* **folderPath**: string (Required): Folder path within the file system.
* **resourceGroup**: string (Required): Resource group of storage account
* **storageAccountName**: string (Required): Storage account name of the source data set
* **subscriptionId**: string (Required): Subscription id of storage account

## BlobProperties
### Properties
* **containerName**: string (Required): Container that has the file path.
* **dataSetId**: string (ReadOnly): Unique id for identifying a data set resource
* **filePath**: string (Required): File path within the source data set
* **resourceGroup**: string (Required): Resource group of storage account
* **storageAccountName**: string (Required): Storage account name of the source data set
* **subscriptionId**: string (Required): Subscription id of storage account

## BlobFolderProperties
### Properties
* **containerName**: string (Required): Container that has the file path.
* **dataSetId**: string (ReadOnly): Unique id for identifying a data set resource
* **prefix**: string (Required): Prefix for blob folder
* **resourceGroup**: string (Required): Resource group of storage account
* **storageAccountName**: string (Required): Storage account name of the source data set
* **subscriptionId**: string (Required): Subscription id of storage account

## BlobContainerProperties
### Properties
* **containerName**: string (Required): BLOB Container name.
* **dataSetId**: string (ReadOnly): Unique id for identifying a data set resource
* **resourceGroup**: string (Required): Resource group of storage account
* **storageAccountName**: string (Required): Storage account name of the source data set
* **subscriptionId**: string (Required): Subscription id of storage account

## KustoClusterDataSetProperties
### Properties
* **dataSetId**: string (ReadOnly): Unique id for identifying a data set resource
* **kustoClusterResourceId**: string (Required): Resource id of the kusto cluster.
* **location**: string (ReadOnly): Location of the kusto cluster.
* **provisioningState**: 'Creating' | 'Deleting' | 'Failed' | 'Moving' | 'Succeeded' (ReadOnly): Provisioning state of the Account

## KustoDatabaseDataSetProperties
### Properties
* **dataSetId**: string (ReadOnly): Unique id for identifying a data set resource
* **kustoDatabaseResourceId**: string (Required): Resource id of the kusto database.
* **location**: string (ReadOnly): Location of the kusto cluster.
* **provisioningState**: 'Creating' | 'Deleting' | 'Failed' | 'Moving' | 'Succeeded' (ReadOnly): Provisioning state of the Account

## SqlDBTableProperties
### Properties
* **databaseName**: string (Required): Database name of the source data set
* **dataSetId**: string (ReadOnly): Unique id for identifying a data set resource
* **schemaName**: string (Required): Schema of the table. Default value is dbo.
* **sqlServerResourceId**: string (Required): Resource id of SQL server
* **tableName**: string (Required): SQL DB table name.

## SqlDWTableProperties
### Properties
* **dataSetId**: string (ReadOnly): Unique id for identifying a data set resource
* **dataWarehouseName**: string (Required): DataWarehouse name of the source data set
* **schemaName**: string (Required): Schema of the table. Default value is dbo.
* **sqlServerResourceId**: string (Required): Resource id of SQL server
* **tableName**: string (Required): SQL DW table name.

## InvitationProperties
### Properties
* **invitationId**: string (ReadOnly): unique invitation id
* **invitationStatus**: 'Accepted' | 'Pending' | 'Rejected' | 'Withdrawn' (ReadOnly): The status of the invitation.
* **respondedAt**: string (ReadOnly): The time the recipient responded to the invitation.
* **sentAt**: string (ReadOnly): Gets the time at which the invitation was sent.
* **targetActiveDirectoryId**: string: The target Azure AD Id. Can't be combined with email.
* **targetEmail**: string: The email the invitation is directed to.
* **targetObjectId**: string: The target user or application Id that invitation is being sent to.
Must be specified along TargetActiveDirectoryId. This enables sending
invitations to specific users or applications in an AD tenant.
* **userEmail**: string (ReadOnly): Email of the user who created the resource
* **userName**: string (ReadOnly): Name of the user who created the resource

## ScheduledSynchronizationSettingProperties
### Properties
* **createdAt**: string (ReadOnly): Time at which the synchronization setting was created.
* **provisioningState**: 'Creating' | 'Deleting' | 'Failed' | 'Moving' | 'Succeeded' (ReadOnly): Provisioning state of the Account
* **recurrenceInterval**: 'Day' | 'Hour' (Required): Recurrence Interval
* **synchronizationTime**: string (Required): Synchronization time
* **userName**: string (ReadOnly): Name of the user who created the synchronization setting.

## ShareSubscriptionProperties
### Properties
* **createdAt**: string (ReadOnly): Time at which the share subscription was created.
* **invitationId**: string (Required): The invitation id.
* **providerEmail**: string (ReadOnly): Email of the provider who created the resource
* **providerName**: string (ReadOnly): Name of the provider who created the resource
* **providerTenantName**: string (ReadOnly): Tenant name of the provider who created the resource
* **provisioningState**: 'Creating' | 'Deleting' | 'Failed' | 'Moving' | 'Succeeded' (ReadOnly): Provisioning state of the Account
* **shareDescription**: string (ReadOnly): Description of share
* **shareKind**: 'CopyBased' | 'InPlace' (ReadOnly): Share kind.
* **shareName**: string (ReadOnly): Name of the share
* **shareSubscriptionStatus**: 'Active' | 'Revoked' | 'Revoking' | 'SourceDeleted' (ReadOnly): Gets the status of share subscription
* **shareTerms**: string (ReadOnly): Terms of a share
* **userEmail**: string (ReadOnly): Email of the user who created the resource
* **userName**: string (ReadOnly): Name of the user who created the resource

## AdlsGen2FileDataSetMappingProperties
### Properties
* **dataSetId**: string (Required): The id of the source data set.
* **dataSetMappingStatus**: 'Broken' | 'Ok' (ReadOnly): Gets the status of the data set mapping.
* **filePath**: string (Required): File path within the file system.
* **fileSystem**: string (Required): File system to which the file belongs.
* **outputType**: 'Csv' | 'Parquet': Type of output file
* **provisioningState**: 'Creating' | 'Deleting' | 'Failed' | 'Moving' | 'Succeeded' (ReadOnly): Provisioning state of the Account
* **resourceGroup**: string (Required): Resource group of storage account.
* **storageAccountName**: string (Required): Storage account name of the source data set.
* **subscriptionId**: string (Required): Subscription id of storage account.

## AdlsGen2FileSystemDataSetMappingProperties
### Properties
* **dataSetId**: string (Required): The id of the source data set.
* **dataSetMappingStatus**: 'Broken' | 'Ok' (ReadOnly): Gets the status of the data set mapping.
* **fileSystem**: string (Required): The file system name.
* **provisioningState**: 'Creating' | 'Deleting' | 'Failed' | 'Moving' | 'Succeeded' (ReadOnly): Provisioning state of the Account
* **resourceGroup**: string (Required): Resource group of storage account.
* **storageAccountName**: string (Required): Storage account name of the source data set.
* **subscriptionId**: string (Required): Subscription id of storage account.

## AdlsGen2FolderDataSetMappingProperties
### Properties
* **dataSetId**: string (Required): The id of the source data set.
* **dataSetMappingStatus**: 'Broken' | 'Ok' (ReadOnly): Gets the status of the data set mapping.
* **fileSystem**: string (Required): File system to which the folder belongs.
* **folderPath**: string (Required): Folder path within the file system.
* **provisioningState**: 'Creating' | 'Deleting' | 'Failed' | 'Moving' | 'Succeeded' (ReadOnly): Provisioning state of the Account
* **resourceGroup**: string (Required): Resource group of storage account.
* **storageAccountName**: string (Required): Storage account name of the source data set.
* **subscriptionId**: string (Required): Subscription id of storage account.

## BlobMappingProperties
### Properties
* **containerName**: string (Required): Container that has the file path.
* **dataSetId**: string (Required): The id of the source data set.
* **dataSetMappingStatus**: 'Broken' | 'Ok' (ReadOnly): Gets the status of the data set mapping.
* **filePath**: string (Required): File path within the source data set
* **outputType**: 'Csv' | 'Parquet': Type of output file
* **provisioningState**: 'Creating' | 'Deleting' | 'Failed' | 'Moving' | 'Succeeded' (ReadOnly): Provisioning state of the Account
* **resourceGroup**: string (Required): Resource group of storage account.
* **storageAccountName**: string (Required): Storage account name of the source data set.
* **subscriptionId**: string (Required): Subscription id of storage account.

## BlobFolderMappingProperties
### Properties
* **containerName**: string (Required): Container that has the file path.
* **dataSetId**: string (Required): The id of the source data set.
* **dataSetMappingStatus**: 'Broken' | 'Ok' (ReadOnly): Gets the status of the data set mapping.
* **prefix**: string (Required): Prefix for blob folder
* **provisioningState**: 'Creating' | 'Deleting' | 'Failed' | 'Moving' | 'Succeeded' (ReadOnly): Provisioning state of the Account
* **resourceGroup**: string (Required): Resource group of storage account.
* **storageAccountName**: string (Required): Storage account name of the source data set.
* **subscriptionId**: string (Required): Subscription id of storage account.

## BlobContainerMappingProperties
### Properties
* **containerName**: string (Required): BLOB Container name.
* **dataSetId**: string (Required): The id of the source data set.
* **dataSetMappingStatus**: 'Broken' | 'Ok' (ReadOnly): Gets the status of the data set mapping.
* **provisioningState**: 'Creating' | 'Deleting' | 'Failed' | 'Moving' | 'Succeeded' (ReadOnly): Provisioning state of the Account
* **resourceGroup**: string (Required): Resource group of storage account.
* **storageAccountName**: string (Required): Storage account name of the source data set.
* **subscriptionId**: string (Required): Subscription id of storage account.

## KustoClusterDataSetMappingProperties
### Properties
* **dataSetId**: string (Required): The id of the source data set.
* **dataSetMappingStatus**: 'Broken' | 'Ok' (ReadOnly): Gets the status of the data set mapping.
* **kustoClusterResourceId**: string (Required): Resource id of the sink kusto cluster.
* **location**: string (ReadOnly): Location of the sink kusto cluster.
* **provisioningState**: 'Creating' | 'Deleting' | 'Failed' | 'Moving' | 'Succeeded' (ReadOnly): Provisioning state of the Account

## KustoDatabaseDataSetMappingProperties
### Properties
* **dataSetId**: string (Required): The id of the source data set.
* **dataSetMappingStatus**: 'Broken' | 'Ok' (ReadOnly): Gets the status of the data set mapping.
* **kustoClusterResourceId**: string (Required): Resource id of the sink kusto cluster.
* **location**: string (ReadOnly): Location of the sink kusto cluster.
* **provisioningState**: 'Creating' | 'Deleting' | 'Failed' | 'Moving' | 'Succeeded' (ReadOnly): Provisioning state of the Account

## SqlDBTableDataSetMappingProperties
### Properties
* **databaseName**: string (Required): DatabaseName name of the sink data set
* **dataSetId**: string (Required): The id of the source data set.
* **dataSetMappingStatus**: 'Broken' | 'Ok' (ReadOnly): Gets the status of the data set mapping.
* **provisioningState**: 'Creating' | 'Deleting' | 'Failed' | 'Moving' | 'Succeeded' (ReadOnly): Provisioning state of the Account
* **schemaName**: string (Required): Schema of the table. Default value is dbo.
* **sqlServerResourceId**: string (Required): Resource id of SQL server
* **tableName**: string (Required): SQL DB table name.

## SqlDWTableDataSetMappingProperties
### Properties
* **dataSetId**: string (Required): The id of the source data set.
* **dataSetMappingStatus**: 'Broken' | 'Ok' (ReadOnly): Gets the status of the data set mapping.
* **dataWarehouseName**: string (Required): DataWarehouse name of the source data set
* **provisioningState**: 'Creating' | 'Deleting' | 'Failed' | 'Moving' | 'Succeeded' (ReadOnly): Provisioning state of the Account
* **schemaName**: string (Required): Schema of the table. Default value is dbo.
* **sqlServerResourceId**: string (Required): Resource id of SQL server
* **tableName**: string (Required): SQL DW table name.

## ScheduledTriggerProperties
### Properties
* **createdAt**: string (ReadOnly): Time at which the trigger was created.
* **provisioningState**: 'Creating' | 'Deleting' | 'Failed' | 'Moving' | 'Succeeded' (ReadOnly): Provisioning state of the Account
* **recurrenceInterval**: 'Day' | 'Hour' (Required): Recurrence Interval
* **synchronizationMode**: 'FullSync' | 'Incremental': Synchronization mode
* **synchronizationTime**: string (Required): Synchronization time
* **triggerStatus**: 'Active' | 'Inactive' | 'SourceSynchronizationSettingDeleted' (ReadOnly): Gets the trigger state
* **userName**: string (ReadOnly): Name of the user who created the trigger.

## SourceShareSynchronizationSettingList
### Properties
* **nextLink**: string (ReadOnly): The Url of next result page.
* **value**: [SourceShareSynchronizationSetting](#sourcesharesynchronizationsetting)[] (ReadOnly): Collection of items of type DataTransferObjects.

## SourceShareSynchronizationSetting
* **Discriminator**: kind

### Base Properties
### ScheduledSourceSynchronizationSetting
#### Properties
* **kind**: 'ScheduleBased' (Required): Kind of synchronization setting on share.
* **properties**: [ScheduledSourceShareSynchronizationSettingProperties](#scheduledsourcesharesynchronizationsettingproperties) (ReadOnly): A Scheduled source synchronization setting data transfer object.


## ScheduledSourceShareSynchronizationSettingProperties
### Properties
* **recurrenceInterval**: 'Day' | 'Hour' (ReadOnly): Recurrence Interval
* **synchronizationTime**: string (ReadOnly): Synchronization time

## ShareSynchronization
### Properties
* **consumerEmail**: string (WriteOnly): Email of the user who created the synchronization
* **consumerName**: string (WriteOnly): Name of the user who created the synchronization
* **consumerTenantName**: string (WriteOnly): Tenant name of the consumer who created the synchronization
* **durationMs**: int (WriteOnly): synchronization duration
* **endTime**: string (WriteOnly): End time of synchronization
* **message**: string (WriteOnly): message of synchronization
* **startTime**: string (WriteOnly): start time of synchronization
* **status**: string (WriteOnly): Raw Status
* **synchronizationId**: string (WriteOnly): Synchronization id
* **synchronizationMode**: 'FullSync' | 'Incremental' (ReadOnly, WriteOnly): Synchronization mode

## SynchronizationDetailsList
### Properties
* **nextLink**: string (ReadOnly): The Url of next result page.
* **value**: [SynchronizationDetails](#synchronizationdetails)[] (ReadOnly): Collection of items of type DataTransferObjects.

## SynchronizationDetails
### Properties
* **dataSetId**: string (ReadOnly): Id of data set
* **dataSetType**: 'AdlsGen1File' | 'AdlsGen1Folder' | 'AdlsGen2File' | 'AdlsGen2FileSystem' | 'AdlsGen2Folder' | 'Blob' | 'BlobFolder' | 'Container' | 'KustoCluster' | 'KustoDatabase' | 'SqlDBTable' | 'SqlDWTable' (ReadOnly): Type of data set
* **durationMs**: int (ReadOnly): Duration of data set level copy
* **endTime**: string (ReadOnly): End time of data set level copy
* **filesRead**: int (ReadOnly): The number of files read from the source data set
* **filesWritten**: int (ReadOnly): The number of files written into the sink data set
* **message**: string (ReadOnly): Error message if any
* **name**: string (ReadOnly): Name of the data set
* **rowsCopied**: int (ReadOnly): The number of files copied into the sink data set
* **rowsRead**: int (ReadOnly): The number of rows read from the source data set.
* **sizeRead**: int (ReadOnly): The size of the data read from the source data set in bytes
* **sizeWritten**: int (ReadOnly): The size of the data written into the sink data set in bytes
* **startTime**: string (ReadOnly): Start time of data set level copy
* **status**: string (ReadOnly): Raw Status
* **vCore**: int (ReadOnly): The vCore units consumed for the data set synchronization

## ShareSubscriptionSynchronization
### Properties
* **durationMs**: int (ReadOnly, WriteOnly): Synchronization duration
* **endTime**: string (ReadOnly, WriteOnly): End time of synchronization
* **message**: string (ReadOnly, WriteOnly): message of Synchronization
* **startTime**: string (ReadOnly, WriteOnly): start time of synchronization
* **status**: string (ReadOnly, WriteOnly): Raw Status
* **synchronizationId**: string (Required, WriteOnly): Synchronization id
* **synchronizationMode**: 'FullSync' | 'Incremental' (ReadOnly, WriteOnly): Synchronization mode

## SynchronizationDetailsList
### Properties
* **nextLink**: string (ReadOnly): The Url of next result page.
* **value**: [SynchronizationDetails](#synchronizationdetails)[] (ReadOnly): Collection of items of type DataTransferObjects.

## ShareSynchronizationList
### Properties
* **nextLink**: string (ReadOnly): The Url of next result page.
* **value**: [ShareSynchronization](#sharesynchronization)[] (ReadOnly): Collection of items of type DataTransferObjects.

## ShareSubscriptionSynchronizationList
### Properties
* **nextLink**: string (ReadOnly): The Url of next result page.
* **value**: [ShareSubscriptionSynchronization](#sharesubscriptionsynchronization)[] (ReadOnly): Collection of items of type DataTransferObjects.

