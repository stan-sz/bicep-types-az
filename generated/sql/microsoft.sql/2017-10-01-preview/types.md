# Microsoft.Sql @ 2017-10-01-preview

## Resource Microsoft.Sql/locations/instanceFailoverGroups@2017-10-01-preview
* **Valid Scope(s)**: ResourceGroup
### Properties
* **apiVersion**: '2017-10-01-preview' (ReadOnly, DeployTimeConstant): The resource api version
* **id**: string (ReadOnly, DeployTimeConstant): The resource id
* **name**: string (Required, DeployTimeConstant): The resource name
* **properties**: [InstanceFailoverGroupProperties](#instancefailovergroupproperties): Properties of a instance failover group.
* **type**: 'Microsoft.Sql/locations/instanceFailoverGroups' (ReadOnly, DeployTimeConstant): The resource type

## Resource Microsoft.Sql/managedInstances/databases/vulnerabilityAssessments@2017-10-01-preview
* **Valid Scope(s)**: ResourceGroup
### Properties
* **apiVersion**: '2017-10-01-preview' (ReadOnly, DeployTimeConstant): The resource api version
* **id**: string (ReadOnly, DeployTimeConstant): The resource id
* **name**: 'default' (Required, DeployTimeConstant): The resource name
* **properties**: [DatabaseVulnerabilityAssessmentProperties](#databasevulnerabilityassessmentproperties): Properties of a database Vulnerability Assessment.
* **type**: 'Microsoft.Sql/managedInstances/databases/vulnerabilityAssessments' (ReadOnly, DeployTimeConstant): The resource type

## Resource Microsoft.Sql/managedInstances/databases/vulnerabilityAssessments/rules/baselines@2017-10-01-preview
* **Valid Scope(s)**: ResourceGroup
### Properties
* **apiVersion**: '2017-10-01-preview' (ReadOnly, DeployTimeConstant): The resource api version
* **id**: string (ReadOnly, DeployTimeConstant): The resource id
* **name**: 'default' | 'master' (Required, DeployTimeConstant): The resource name
* **properties**: [DatabaseVulnerabilityAssessmentRuleBaselineProperties](#databasevulnerabilityassessmentrulebaselineproperties): Properties of a database Vulnerability Assessment rule baseline.
* **type**: 'Microsoft.Sql/managedInstances/databases/vulnerabilityAssessments/rules/baselines' (ReadOnly, DeployTimeConstant): The resource type

## Resource Microsoft.Sql/managedInstances/encryptionProtector@2017-10-01-preview
* **Valid Scope(s)**: ResourceGroup
### Properties
* **apiVersion**: '2017-10-01-preview' (ReadOnly, DeployTimeConstant): The resource api version
* **id**: string (ReadOnly, DeployTimeConstant): The resource id
* **kind**: string (ReadOnly): Kind of encryption protector. This is metadata used for the Azure portal experience.
* **name**: 'current' (Required, DeployTimeConstant): The resource name
* **properties**: [ManagedInstanceEncryptionProtectorProperties](#managedinstanceencryptionprotectorproperties): Properties for an encryption protector execution.
* **type**: 'Microsoft.Sql/managedInstances/encryptionProtector' (ReadOnly, DeployTimeConstant): The resource type

## Resource Microsoft.Sql/managedInstances/keys@2017-10-01-preview
* **Valid Scope(s)**: ResourceGroup
### Properties
* **apiVersion**: '2017-10-01-preview' (ReadOnly, DeployTimeConstant): The resource api version
* **id**: string (ReadOnly, DeployTimeConstant): The resource id
* **kind**: string (ReadOnly): Kind of encryption protector. This is metadata used for the Azure portal experience.
* **name**: string (Required, DeployTimeConstant): The resource name
* **properties**: [ManagedInstanceKeyProperties](#managedinstancekeyproperties): Properties for a key execution.
* **type**: 'Microsoft.Sql/managedInstances/keys' (ReadOnly, DeployTimeConstant): The resource type

## Resource Microsoft.Sql/servers/databases@2017-10-01-preview
* **Valid Scope(s)**: ResourceGroup
### Properties
* **apiVersion**: '2017-10-01-preview' (ReadOnly, DeployTimeConstant): The resource api version
* **id**: string (ReadOnly, DeployTimeConstant): The resource id
* **kind**: string (ReadOnly): Kind of database. This is metadata used for the Azure portal experience.
* **location**: string (Required): Resource location.
* **managedBy**: string (ReadOnly): Resource that manages the database.
* **name**: string (Required, DeployTimeConstant): The resource name
* **properties**: [DatabaseProperties](#databaseproperties): The database's properties.
* **sku**: [Sku](#sku): An ARM Resource SKU.
* **tags**: [TrackedResourceTags](#trackedresourcetags): Resource tags.
* **type**: 'Microsoft.Sql/servers/databases' (ReadOnly, DeployTimeConstant): The resource type

## Resource Microsoft.Sql/servers/databases/backupShortTermRetentionPolicies@2017-10-01-preview
* **Valid Scope(s)**: ResourceGroup
### Properties
* **apiVersion**: '2017-10-01-preview' (ReadOnly, DeployTimeConstant): The resource api version
* **id**: string (ReadOnly, DeployTimeConstant): The resource id
* **name**: 'default' (Required, DeployTimeConstant): The resource name
* **properties**: [BackupShortTermRetentionPolicyProperties](#backupshorttermretentionpolicyproperties): Properties of a short term retention policy
* **type**: 'Microsoft.Sql/servers/databases/backupShortTermRetentionPolicies' (ReadOnly, DeployTimeConstant): The resource type

## Resource Microsoft.Sql/servers/elasticPools@2017-10-01-preview
* **Valid Scope(s)**: ResourceGroup
### Properties
* **apiVersion**: '2017-10-01-preview' (ReadOnly, DeployTimeConstant): The resource api version
* **id**: string (ReadOnly, DeployTimeConstant): The resource id
* **kind**: string (ReadOnly): Kind of elastic pool. This is metadata used for the Azure portal experience.
* **location**: string (Required): Resource location.
* **name**: string (Required, DeployTimeConstant): The resource name
* **properties**: [ElasticPoolProperties](#elasticpoolproperties): Properties of an elastic pool
* **sku**: [Sku](#sku): An ARM Resource SKU.
* **tags**: [TrackedResourceTags](#trackedresourcetags): Resource tags.
* **type**: 'Microsoft.Sql/servers/elasticPools' (ReadOnly, DeployTimeConstant): The resource type

## InstanceFailoverGroupProperties
### Properties
* **managedInstancePairs**: [ManagedInstancePairInfo](#managedinstancepairinfo)[] (Required): List of managed instance pairs in the failover group.
* **partnerRegions**: [PartnerRegionInfo](#partnerregioninfo)[] (Required): Partner region information for the failover group.
* **readOnlyEndpoint**: [InstanceFailoverGroupReadOnlyEndpoint](#instancefailovergroupreadonlyendpoint): Read-only endpoint of the failover group instance.
* **readWriteEndpoint**: [InstanceFailoverGroupReadWriteEndpoint](#instancefailovergroupreadwriteendpoint) (Required): Read-write endpoint of the failover group instance.
* **replicationRole**: 'Primary' | 'Secondary' (ReadOnly): Local replication role of the failover group instance.
* **replicationState**: string (ReadOnly): Replication state of the failover group instance.

## ManagedInstancePairInfo
### Properties
* **partnerManagedInstanceId**: string: Id of Partner Managed Instance in pair.
* **primaryManagedInstanceId**: string: Id of Primary Managed Instance in pair.

## PartnerRegionInfo
### Properties
* **location**: string: Geo location of the partner managed instances.
* **replicationRole**: 'Primary' | 'Secondary' (ReadOnly): Local replication role of the failover group instance.

## InstanceFailoverGroupReadOnlyEndpoint
### Properties
* **failoverPolicy**: 'Disabled' | 'Enabled': Failover policy of the read-only endpoint for the failover group.

## InstanceFailoverGroupReadWriteEndpoint
### Properties
* **failoverPolicy**: 'Automatic' | 'Manual' (Required): Failover policy of the read-write endpoint for the failover group. If failoverPolicy is Automatic then failoverWithDataLossGracePeriodMinutes is required.
* **failoverWithDataLossGracePeriodMinutes**: int: Grace period before failover with data loss is attempted for the read-write endpoint. If failoverPolicy is Automatic then failoverWithDataLossGracePeriodMinutes is required.

## DatabaseVulnerabilityAssessmentProperties
### Properties
* **recurringScans**: [VulnerabilityAssessmentRecurringScansProperties](#vulnerabilityassessmentrecurringscansproperties): Properties of a Vulnerability Assessment recurring scans.
* **storageAccountAccessKey**: string (WriteOnly): Specifies the identifier key of the storage account for vulnerability assessment scan results. If 'StorageContainerSasKey' isn't specified, storageAccountAccessKey is required.
* **storageContainerPath**: string (WriteOnly): A blob storage container path to hold the scan results (e.g. https://myStorage.blob.core.windows.net/VaScans/).  It is required if server level vulnerability assessment policy doesn't set
* **storageContainerSasKey**: string (WriteOnly): A shared access signature (SAS Key) that has read and write access to the blob container specified in 'storageContainerPath' parameter. If 'storageAccountAccessKey' isn't specified, StorageContainerSasKey is required.

## VulnerabilityAssessmentRecurringScansProperties
### Properties
* **emails**: string[]: Specifies an array of e-mail addresses to which the scan notification is sent.
* **emailSubscriptionAdmins**: bool: Specifies that the schedule scan notification will be is sent to the subscription administrators.
* **isEnabled**: bool: Recurring scans state.

## DatabaseVulnerabilityAssessmentRuleBaselineProperties
### Properties
* **baselineResults**: [DatabaseVulnerabilityAssessmentRuleBaselineItem](#databasevulnerabilityassessmentrulebaselineitem)[] (Required): The rule baseline result

## DatabaseVulnerabilityAssessmentRuleBaselineItem
### Properties
* **result**: string[] (Required): The rule baseline result

## ManagedInstanceEncryptionProtectorProperties
### Properties
* **serverKeyName**: string: The name of the managed instance key.
* **serverKeyType**: 'AzureKeyVault' | 'ServiceManaged' (Required): The key type like 'ServiceManaged', 'AzureKeyVault'.
* **thumbprint**: string (ReadOnly): Thumbprint of the server key.
* **uri**: string (ReadOnly): The URI of the server key.

## ManagedInstanceKeyProperties
### Properties
* **creationDate**: string (ReadOnly): The key creation date.
* **serverKeyType**: 'AzureKeyVault' | 'ServiceManaged' (Required, WriteOnly): The key type like 'ServiceManaged', 'AzureKeyVault'.
* **thumbprint**: string (ReadOnly): Thumbprint of the key.
* **uri**: string (WriteOnly): The URI of the key. If the ServerKeyType is AzureKeyVault, then the URI is required.

## DatabaseProperties
### Properties
* **autoPauseDelay**: int: Time in minutes after which database is automatically paused. A value of -1 means that automatic pause is disabled
* **catalogCollation**: 'DATABASE_DEFAULT' | 'SQL_Latin1_General_CP1_CI_AS': Collation of the metadata catalog.
* **collation**: string: The collation of the database.
* **createMode**: 'Copy' | 'Default' | 'OnlineSecondary' | 'PointInTimeRestore' | 'Recovery' | 'Restore' | 'RestoreExternalBackup' | 'RestoreExternalBackupSecondary' | 'RestoreLongTermRetentionBackup' | 'Secondary' (WriteOnly): Specifies the mode of database creation.

Default: regular database creation.

Copy: creates a database as a copy of an existing database. sourceDatabaseId must be specified as the resource ID of the source database.

Secondary: creates a database as a secondary replica of an existing database. sourceDatabaseId must be specified as the resource ID of the existing primary database.

PointInTimeRestore: Creates a database by restoring a point in time backup of an existing database. sourceDatabaseId must be specified as the resource ID of the existing database, and restorePointInTime must be specified.

Recovery: Creates a database by restoring a geo-replicated backup. sourceDatabaseId must be specified as the recoverable database resource ID to restore.

Restore: Creates a database by restoring a backup of a deleted database. sourceDatabaseId must be specified. If sourceDatabaseId is the database's original resource ID, then sourceDatabaseDeletionDate must be specified. Otherwise sourceDatabaseId must be the restorable dropped database resource ID and sourceDatabaseDeletionDate is ignored. restorePointInTime may also be specified to restore from an earlier point in time.

RestoreLongTermRetentionBackup: Creates a database by restoring from a long term retention vault. recoveryServicesRecoveryPointResourceId must be specified as the recovery point resource ID.

Copy, Secondary, and RestoreLongTermRetentionBackup are not supported for DataWarehouse edition.
* **creationDate**: string (ReadOnly): The creation date of the database (ISO8601 format).
* **currentServiceObjectiveName**: string (ReadOnly): The current service level objective name of the database.
* **currentSku**: [Sku](#sku) (ReadOnly): An ARM Resource SKU.
* **databaseId**: string (ReadOnly): The ID of the database.
* **defaultSecondaryLocation**: string (ReadOnly): The default secondary region for this database.
* **earliestRestoreDate**: string (ReadOnly): This records the earliest start date and time that restore is available for this database (ISO8601 format).
* **elasticPoolId**: string: The resource identifier of the elastic pool containing this database.
* **failoverGroupId**: string (ReadOnly): Failover Group resource identifier that this database belongs to.
* **licenseType**: 'BasePrice' | 'LicenseIncluded': The license type to apply for this database. `LicenseIncluded` if you need a license, or `BasePrice` if you have a license and are eligible for the Azure Hybrid Benefit.
* **longTermRetentionBackupResourceId**: string (WriteOnly): The resource identifier of the long term retention backup associated with create operation of this database.
* **maxLogSizeBytes**: int (ReadOnly): The max log size for this database.
* **maxSizeBytes**: int: The max size of the database expressed in bytes.
* **minCapacity**: int: Minimal capacity that database will always have allocated, if not paused
* **pausedDate**: string (ReadOnly): The date when database was paused by user configuration or action (ISO8601 format). Null if the database is ready.
* **readReplicaCount**: int: The number of readonly secondary replicas associated with the database to which readonly application intent connections may be routed. This property is only settable for Hyperscale edition databases.
* **readScale**: 'Disabled' | 'Enabled': If enabled, connections that have application intent set to readonly in their connection string may be routed to a readonly secondary replica. This property is only settable for Premium and Business Critical databases.
* **recoverableDatabaseId**: string (WriteOnly): The resource identifier of the recoverable database associated with create operation of this database.
* **recoveryServicesRecoveryPointId**: string (WriteOnly): The resource identifier of the recovery point associated with create operation of this database.
* **requestedServiceObjectiveName**: string (ReadOnly): The requested service level objective name of the database.
* **restorableDroppedDatabaseId**: string (WriteOnly): The resource identifier of the restorable dropped database associated with create operation of this database.
* **restorePointInTime**: string (WriteOnly): Specifies the point in time (ISO8601 format) of the source database that will be restored to create the new database.
* **resumedDate**: string (ReadOnly): The date when database was resumed by user action or database login (ISO8601 format). Null if the database is paused.
* **sampleName**: 'AdventureWorksLT' | 'WideWorldImportersFull' | 'WideWorldImportersStd' (WriteOnly): The name of the sample schema to apply when creating this database.
* **sourceDatabaseDeletionDate**: string (WriteOnly): Specifies the time that the database was deleted.
* **sourceDatabaseId**: string (WriteOnly): The resource identifier of the source database associated with create operation of this database.
* **status**: 'AutoClosed' | 'Copying' | 'Creating' | 'Disabled' | 'EmergencyMode' | 'Inaccessible' | 'Offline' | 'OfflineChangingDwPerformanceTiers' | 'OfflineSecondary' | 'Online' | 'OnlineChangingDwPerformanceTiers' | 'Paused' | 'Pausing' | 'Recovering' | 'RecoveryPending' | 'Restoring' | 'Resuming' | 'Scaling' | 'Shutdown' | 'Standby' | 'Suspect' (ReadOnly): The status of the database.
* **zoneRedundant**: bool: Whether or not this database is zone redundant, which means the replicas of this database will be spread across multiple availability zones.

## Sku
### Properties
* **capacity**: int: Capacity of the particular SKU.
* **family**: string: If the service has different generations of hardware, for the same SKU, then that can be captured here.
* **name**: string (Required): The name of the SKU, typically, a letter + Number code, e.g. P3.
* **size**: string: Size of the particular SKU
* **tier**: string: The tier or edition of the particular SKU, e.g. Basic, Premium.

## TrackedResourceTags
### Properties
### Additional Properties
* **Additional Properties Type**: string

## BackupShortTermRetentionPolicyProperties
### Properties
* **retentionDays**: int: The backup retention period in days. This is how many days Point-in-Time Restore will be supported.

## ElasticPoolProperties
### Properties
* **creationDate**: string (ReadOnly): The creation date of the elastic pool (ISO8601 format).
* **licenseType**: 'BasePrice' | 'LicenseIncluded': The license type to apply for this elastic pool.
* **maxSizeBytes**: int: The storage limit for the database elastic pool in bytes.
* **perDatabaseSettings**: [ElasticPoolPerDatabaseSettings](#elasticpoolperdatabasesettings): Per database settings of an elastic pool.
* **state**: 'Creating' | 'Disabled' | 'Ready' (ReadOnly): The state of the elastic pool.
* **zoneRedundant**: bool: Whether or not this elastic pool is zone redundant, which means the replicas of this elastic pool will be spread across multiple availability zones.

## ElasticPoolPerDatabaseSettings
### Properties
* **maxCapacity**: int: The maximum capacity any one database can consume.
* **minCapacity**: int: The minimum capacity all databases are guaranteed.

## TrackedResourceTags
### Properties
### Additional Properties
* **Additional Properties Type**: string

