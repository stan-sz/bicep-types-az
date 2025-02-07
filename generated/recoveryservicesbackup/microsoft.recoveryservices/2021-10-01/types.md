# Microsoft.RecoveryServices @ 2021-10-01

## Resource Microsoft.RecoveryServices/vaults/backupconfig@2021-10-01
* **Valid Scope(s)**: ResourceGroup
### Properties
* **apiVersion**: '2021-10-01' (ReadOnly, DeployTimeConstant): The resource api version
* **eTag**: string: Optional ETag.
* **id**: string (ReadOnly, DeployTimeConstant): The resource id
* **location**: string: Resource location.
* **name**: 'vaultconfig' (Required, DeployTimeConstant): The resource name
* **properties**: [BackupResourceVaultConfig](#backupresourcevaultconfig): Backup resource vault config details.
* **tags**: [ResourceTags](#resourcetags): Resource tags.
* **type**: 'Microsoft.RecoveryServices/vaults/backupconfig' (ReadOnly, DeployTimeConstant): The resource type

## Resource Microsoft.RecoveryServices/vaults/backupEncryptionConfigs@2021-10-01
* **Valid Scope(s)**: ResourceGroup
### Properties
* **apiVersion**: '2021-10-01' (ReadOnly, DeployTimeConstant): The resource api version
* **eTag**: string: Optional ETag.
* **id**: string (ReadOnly, DeployTimeConstant): The resource id
* **location**: string: Resource location.
* **name**: 'backupResourceEncryptionConfig' (Required, DeployTimeConstant): The resource name
* **properties**: [BackupResourceEncryptionConfig](#backupresourceencryptionconfig)
* **tags**: [ResourceTags](#resourcetags): Resource tags.
* **type**: 'Microsoft.RecoveryServices/vaults/backupEncryptionConfigs' (ReadOnly, DeployTimeConstant): The resource type

## Resource Microsoft.RecoveryServices/vaults/backupFabrics/backupProtectionIntent@2021-10-01
* **Valid Scope(s)**: ResourceGroup
### Properties
* **apiVersion**: '2021-10-01' (ReadOnly, DeployTimeConstant): The resource api version
* **eTag**: string: Optional ETag.
* **id**: string (ReadOnly, DeployTimeConstant): The resource id
* **location**: string: Resource location.
* **name**: string (Required, DeployTimeConstant): The resource name
* **properties**: [ProtectionIntent](#protectionintent): Base class for backup ProtectionIntent.
* **tags**: [ResourceTags](#resourcetags): Resource tags.
* **type**: 'Microsoft.RecoveryServices/vaults/backupFabrics/backupProtectionIntent' (ReadOnly, DeployTimeConstant): The resource type

## Resource Microsoft.RecoveryServices/vaults/backupFabrics/protectionContainers@2021-10-01
* **Valid Scope(s)**: ResourceGroup
### Properties
* **apiVersion**: '2021-10-01' (ReadOnly, DeployTimeConstant): The resource api version
* **eTag**: string: Optional ETag.
* **id**: string (ReadOnly, DeployTimeConstant): The resource id
* **location**: string: Resource location.
* **name**: string (Required, DeployTimeConstant): The resource name
* **properties**: [ProtectionContainer](#protectioncontainer): Base class for container with backup items. Containers with specific workloads are derived from this class.
* **tags**: [ResourceTags](#resourcetags): Resource tags.
* **type**: 'Microsoft.RecoveryServices/vaults/backupFabrics/protectionContainers' (ReadOnly, DeployTimeConstant): The resource type

## Resource Microsoft.RecoveryServices/vaults/backupFabrics/protectionContainers/protectedItems@2021-10-01
* **Valid Scope(s)**: ResourceGroup
### Properties
* **apiVersion**: '2021-10-01' (ReadOnly, DeployTimeConstant): The resource api version
* **eTag**: string: Optional ETag.
* **id**: string (ReadOnly, DeployTimeConstant): The resource id
* **location**: string: Resource location.
* **name**: string (Required, DeployTimeConstant): The resource name
* **properties**: [ProtectedItem](#protecteditem): Base class for backup items.
* **tags**: [ResourceTags](#resourcetags): Resource tags.
* **type**: 'Microsoft.RecoveryServices/vaults/backupFabrics/protectionContainers/protectedItems' (ReadOnly, DeployTimeConstant): The resource type

## Resource Microsoft.RecoveryServices/vaults/backupPolicies@2021-10-01
* **Valid Scope(s)**: ResourceGroup
### Properties
* **apiVersion**: '2021-10-01' (ReadOnly, DeployTimeConstant): The resource api version
* **eTag**: string: Optional ETag.
* **id**: string (ReadOnly, DeployTimeConstant): The resource id
* **location**: string: Resource location.
* **name**: string (Required, DeployTimeConstant): The resource name
* **properties**: [ProtectionPolicy](#protectionpolicy): Base class for backup policy. Workload-specific backup policies are derived from this class.
* **tags**: [ResourceTags](#resourcetags): Resource tags.
* **type**: 'Microsoft.RecoveryServices/vaults/backupPolicies' (ReadOnly, DeployTimeConstant): The resource type

## Resource Microsoft.RecoveryServices/vaults/backupResourceGuardProxies@2021-10-01
* **Valid Scope(s)**: ResourceGroup
### Properties
* **apiVersion**: '2021-10-01' (ReadOnly, DeployTimeConstant): The resource api version
* **eTag**: string (ReadOnly): Optional ETag.
* **id**: string (ReadOnly, DeployTimeConstant): The resource id
* **location**: string (ReadOnly): Resource location.
* **name**: string (Required, DeployTimeConstant): The resource name
* **properties**: [ResourceGuardProxyBase](#resourceguardproxybase) (ReadOnly)
* **tags**: [ResourceTags](#resourcetags) (ReadOnly): Resource tags.
* **type**: 'Microsoft.RecoveryServices/vaults/backupResourceGuardProxies' (ReadOnly, DeployTimeConstant): The resource type

## Resource Microsoft.RecoveryServices/vaults/backupstorageconfig@2021-10-01
* **Valid Scope(s)**: ResourceGroup
### Properties
* **apiVersion**: '2021-10-01' (ReadOnly, DeployTimeConstant): The resource api version
* **eTag**: string: Optional ETag.
* **id**: string (ReadOnly, DeployTimeConstant): The resource id
* **location**: string: Resource location.
* **name**: 'vaultstorageconfig' (Required, DeployTimeConstant): The resource name
* **properties**: [BackupResourceConfig](#backupresourceconfig): The resource storage details.
* **tags**: [ResourceTags](#resourcetags): Resource tags.
* **type**: 'Microsoft.RecoveryServices/vaults/backupstorageconfig' (ReadOnly, DeployTimeConstant): The resource type

## Resource Microsoft.RecoveryServices/vaults/privateEndpointConnections@2021-10-01
* **Valid Scope(s)**: ResourceGroup
### Properties
* **apiVersion**: '2021-10-01' (ReadOnly, DeployTimeConstant): The resource api version
* **eTag**: string: Optional ETag.
* **id**: string (ReadOnly, DeployTimeConstant): The resource id
* **location**: string: Resource location.
* **name**: string (Required, DeployTimeConstant): The resource name
* **properties**: [PrivateEndpointConnection](#privateendpointconnection): Private Endpoint Connection Response Properties
* **tags**: [ResourceTags](#resourcetags): Resource tags.
* **type**: 'Microsoft.RecoveryServices/vaults/privateEndpointConnections' (ReadOnly, DeployTimeConstant): The resource type

## BackupResourceVaultConfig
### Properties
* **enhancedSecurityState**: 'Disabled' | 'Enabled' | 'Invalid': Enabled or Disabled.
* **isSoftDeleteFeatureStateEditable**: bool: Is soft delete feature state editable
* **resourceGuardOperationRequests**: string[]: ResourceGuard Operation Requests
* **softDeleteFeatureState**: 'Disabled' | 'Enabled' | 'Invalid': Soft Delete feature state
* **storageModelType**: 'GeoRedundant' | 'Invalid' | 'LocallyRedundant' | 'ReadAccessGeoZoneRedundant' | 'ZoneRedundant': Storage type
* **storageType**: 'GeoRedundant' | 'Invalid' | 'LocallyRedundant' | 'ReadAccessGeoZoneRedundant' | 'ZoneRedundant': Storage type
* **storageTypeState**: 'Invalid' | 'Locked' | 'Unlocked': Locked or Unlocked. Once a machine is registered against a resource, the storageTypeState is always Locked.

## ResourceTags
### Properties
### Additional Properties
* **Additional Properties Type**: string

## BackupResourceEncryptionConfig
### Properties
* **encryptionAtRestType**: 'CustomerManaged' | 'Invalid' | 'MicrosoftManaged': Encryption At Rest Type
* **infrastructureEncryptionState**: 'Disabled' | 'Enabled' | 'Invalid'
* **keyUri**: string: Key Vault Key URI
* **lastUpdateStatus**: 'Failed' | 'FirstInitialization' | 'Initialized' | 'Invalid' | 'NotEnabled' | 'PartiallyFailed' | 'PartiallySucceeded' | 'Succeeded'
* **subscriptionId**: string: Key Vault Subscription Id
* **userAssignedIdentity**: string (ReadOnly): User Assigned Identity Id
* **useSystemAssignedIdentity**: bool (ReadOnly): bool to indicate whether to use system Assigned Identity or not

## ResourceTags
### Properties
### Additional Properties
* **Additional Properties Type**: string

## ProtectionIntent
* **Discriminator**: protectionIntentItemType

### Base Properties
* **backupManagementType**: 'AzureBackupServer' | 'AzureIaasVM' | 'AzureSql' | 'AzureStorage' | 'AzureWorkload' | 'DPM' | 'DefaultBackup' | 'Invalid' | 'MAB': Backup management type to execute the current job.
* **itemId**: string: ID of the item which is getting protected, In case of Azure Vm , it is ProtectedItemId
* **policyId**: string: ID of the backup policy with which this item is backed up.
* **protectionState**: 'Invalid' | 'NotProtected' | 'Protected' | 'Protecting' | 'ProtectionFailed': Specifies whether the container is registered or not
* **sourceResourceId**: string: ARM ID of the resource to be backed up.
### AzureResourceProtectionIntent
#### Properties
* **friendlyName**: string: Friendly name of the VM represented by this backup item.
* **protectionIntentItemType**: 'AzureResourceItem' (Required): backup protectionIntent type.

### AzureWorkloadContainerAutoProtectionIntent
#### Properties
* **protectionIntentItemType**: 'AzureWorkloadContainerAutoProtectionIntent' (Required): backup protectionIntent type.

### AzureWorkloadSQLAutoProtectionIntent
#### Properties
* **protectionIntentItemType**: 'AzureWorkloadSQLAutoProtectionIntent' (Required): backup protectionIntent type.
* **workloadItemType**: 'Invalid' | 'SAPAseDatabase' | 'SAPAseSystem' | 'SAPHanaDatabase' | 'SAPHanaSystem' | 'SQLDataBase' | 'SQLInstance': Workload item type of the item for which intent is to be set


## ResourceTags
### Properties
### Additional Properties
* **Additional Properties Type**: string

## ProtectionContainer
* **Discriminator**: containerType

### Base Properties
* **backupManagementType**: 'AzureBackupServer' | 'AzureIaasVM' | 'AzureSql' | 'AzureStorage' | 'AzureWorkload' | 'DPM' | 'DefaultBackup' | 'Invalid' | 'MAB': Backup management type to execute the current job.
* **friendlyName**: string: Friendly name of the container.
* **healthStatus**: string: Status of health of the container.
* **protectableObjectType**: string: Type of the protectable object associated with this container
* **registrationStatus**: string: Status of registration of the container with the Recovery Services Vault.
### AzureBackupServerContainer
#### Properties
* **containerType**: 'AzureBackupServerContainer' (Required): Type of the container. The value of this property for: 1. Compute Azure VM is Microsoft.Compute/virtualMachines 2.
Classic Compute Azure VM is Microsoft.ClassicCompute/virtualMachines 3. Windows machines (like MAB, DPM etc) is
Windows 4. Azure SQL instance is AzureSqlContainer. 5. Storage containers is StorageContainer. 6. Azure workload
Backup is VMAppContainer

### AzureSqlContainer
#### Properties
* **containerType**: 'AzureSqlContainer' (Required): Type of the container. The value of this property for: 1. Compute Azure VM is Microsoft.Compute/virtualMachines 2.
Classic Compute Azure VM is Microsoft.ClassicCompute/virtualMachines 3. Windows machines (like MAB, DPM etc) is
Windows 4. Azure SQL instance is AzureSqlContainer. 5. Storage containers is StorageContainer. 6. Azure workload
Backup is VMAppContainer

### GenericContainer
#### Properties
* **containerType**: 'GenericContainer' (Required): Type of the container. The value of this property for: 1. Compute Azure VM is Microsoft.Compute/virtualMachines 2.
Classic Compute Azure VM is Microsoft.ClassicCompute/virtualMachines 3. Windows machines (like MAB, DPM etc) is
Windows 4. Azure SQL instance is AzureSqlContainer. 5. Storage containers is StorageContainer. 6. Azure workload
Backup is VMAppContainer
* **extendedInformation**: [GenericContainerExtendedInfo](#genericcontainerextendedinfo): Container extended information
* **fabricName**: string: Name of the container's fabric

### AzureIaaSClassicComputeVMContainer
#### Properties
* **containerType**: 'Microsoft.ClassicCompute/virtualMachines' (Required): Type of the container. The value of this property for: 1. Compute Azure VM is Microsoft.Compute/virtualMachines 2.
Classic Compute Azure VM is Microsoft.ClassicCompute/virtualMachines 3. Windows machines (like MAB, DPM etc) is
Windows 4. Azure SQL instance is AzureSqlContainer. 5. Storage containers is StorageContainer. 6. Azure workload
Backup is VMAppContainer

### AzureIaaSComputeVMContainer
#### Properties
* **containerType**: 'Microsoft.Compute/virtualMachines' (Required): Type of the container. The value of this property for: 1. Compute Azure VM is Microsoft.Compute/virtualMachines 2.
Classic Compute Azure VM is Microsoft.ClassicCompute/virtualMachines 3. Windows machines (like MAB, DPM etc) is
Windows 4. Azure SQL instance is AzureSqlContainer. 5. Storage containers is StorageContainer. 6. Azure workload
Backup is VMAppContainer

### AzureSqlagWorkloadContainerProtectionContainer
#### Properties
* **containerType**: 'SQLAGWorkLoadContainer' (Required): Type of the container. The value of this property for: 1. Compute Azure VM is Microsoft.Compute/virtualMachines 2.
Classic Compute Azure VM is Microsoft.ClassicCompute/virtualMachines 3. Windows machines (like MAB, DPM etc) is
Windows 4. Azure SQL instance is AzureSqlContainer. 5. Storage containers is StorageContainer. 6. Azure workload
Backup is VMAppContainer

### AzureStorageContainer
#### Properties
* **acquireStorageAccountLock**: 'Acquire' | 'NotAcquire': Whether storage account lock is to be acquired for this container or not.
* **containerType**: 'StorageContainer' (Required): Type of the container. The value of this property for: 1. Compute Azure VM is Microsoft.Compute/virtualMachines 2.
Classic Compute Azure VM is Microsoft.ClassicCompute/virtualMachines 3. Windows machines (like MAB, DPM etc) is
Windows 4. Azure SQL instance is AzureSqlContainer. 5. Storage containers is StorageContainer. 6. Azure workload
Backup is VMAppContainer
* **protectedItemCount**: int: Number of items backed up in this container.
* **resourceGroup**: string: Resource group name of Recovery Services Vault.
* **sourceResourceId**: string: Fully qualified ARM url.
* **storageAccountVersion**: string: Storage account version.

### AzureVMAppContainerProtectionContainer
#### Properties
* **containerType**: 'VMAppContainer' (Required): Type of the container. The value of this property for: 1. Compute Azure VM is Microsoft.Compute/virtualMachines 2.
Classic Compute Azure VM is Microsoft.ClassicCompute/virtualMachines 3. Windows machines (like MAB, DPM etc) is
Windows 4. Azure SQL instance is AzureSqlContainer. 5. Storage containers is StorageContainer. 6. Azure workload
Backup is VMAppContainer

### MabContainer
#### Properties
* **agentVersion**: string: Agent version of this container.
* **canReRegister**: bool: Can the container be registered one more time.
* **containerHealthState**: string: Health state of mab container.
* **containerId**: int: ContainerID represents the container.
* **containerType**: 'Windows' (Required): Type of the container. The value of this property for: 1. Compute Azure VM is Microsoft.Compute/virtualMachines 2.
Classic Compute Azure VM is Microsoft.ClassicCompute/virtualMachines 3. Windows machines (like MAB, DPM etc) is
Windows 4. Azure SQL instance is AzureSqlContainer. 5. Storage containers is StorageContainer. 6. Azure workload
Backup is VMAppContainer
* **extendedInfo**: [MabContainerExtendedInfo](#mabcontainerextendedinfo): Additional information of the container.
* **mabContainerHealthDetails**: [MABContainerHealthDetails](#mabcontainerhealthdetails)[]: Health details on this mab container.
* **protectedItemCount**: int: Number of items backed up in this container.


## GenericContainerExtendedInfo
### Properties
* **containerIdentityInfo**: [ContainerIdentityInfo](#containeridentityinfo): Container identity information
* **rawCertData**: string: Public key of container cert
* **serviceEndpoints**: [GenericContainerExtendedInfoServiceEndpoints](#genericcontainerextendedinfoserviceendpoints): Azure Backup Service Endpoints for the container

## ContainerIdentityInfo
### Properties
* **aadTenantId**: string: Protection container identity - AAD Tenant
* **audience**: string: Protection container identity - Audience
* **servicePrincipalClientId**: string: Protection container identity - AAD Service Principal
* **uniqueName**: string: Unique name of the container

## GenericContainerExtendedInfoServiceEndpoints
### Properties
### Additional Properties
* **Additional Properties Type**: string

## MabContainerExtendedInfo
### Properties
* **backupItems**: string[]: List of backup items associated with this container.
* **backupItemType**: 'AzureFileShare' | 'AzureSqlDb' | 'Client' | 'Exchange' | 'FileFolder' | 'GenericDataSource' | 'Invalid' | 'SAPAseDatabase' | 'SAPHanaDatabase' | 'SQLDB' | 'SQLDataBase' | 'Sharepoint' | 'SystemState' | 'VM' | 'VMwareVM': Type of backup items associated with this container.
* **lastBackupStatus**: string: Latest backup status of this container.
* **lastRefreshedAt**: string: Time stamp when this container was refreshed.
* **policyName**: string: Backup policy associated with this container.

## MABContainerHealthDetails
### Properties
* **code**: int: Health Code
* **message**: string: Health Message
* **recommendations**: string[]: Health Recommended Actions
* **title**: string: Health Title

## ResourceTags
### Properties
### Additional Properties
* **Additional Properties Type**: string

## ProtectedItem
* **Discriminator**: protectedItemType

### Base Properties
* **backupManagementType**: 'AzureBackupServer' | 'AzureIaasVM' | 'AzureSql' | 'AzureStorage' | 'AzureWorkload' | 'DPM' | 'DefaultBackup' | 'Invalid' | 'MAB': Backup management type to execute the current job.
* **backupSetName**: string: Name of the backup set the backup item belongs to
* **containerName**: string: Unique name of container
* **createMode**: 'Default' | 'Invalid' | 'Recover': Create mode to indicate recovery of existing soft deleted data source or creation of new data source.
* **deferredDeleteTimeInUTC**: string: Time for deferred deletion in UTC
* **deferredDeleteTimeRemaining**: string: Time remaining before the DS marked for deferred delete is permanently deleted
* **isArchiveEnabled**: bool: Flag to identify whether datasource is protected in archive
* **isDeferredDeleteScheduleUpcoming**: bool: Flag to identify whether the deferred deleted DS is to be purged soon
* **isRehydrate**: bool: Flag to identify that deferred deleted DS is to be moved into Pause state
* **isScheduledForDeferredDelete**: bool: Flag to identify whether the DS is scheduled for deferred delete
* **lastRecoveryPoint**: string: Timestamp when the last (latest) backup copy was created for this backup item.
* **policyId**: string: ID of the backup policy with which this item is backed up.
* **policyName**: string: Name of the policy used for protection
* **resourceGuardOperationRequests**: string[]: ResourceGuardOperationRequests on which LAC check will be performed
* **sourceResourceId**: string: ARM ID of the resource to be backed up.
* **workloadType**: 'AzureFileShare' | 'AzureSqlDb' | 'Client' | 'Exchange' | 'FileFolder' | 'GenericDataSource' | 'Invalid' | 'SAPAseDatabase' | 'SAPHanaDatabase' | 'SQLDB' | 'SQLDataBase' | 'Sharepoint' | 'SystemState' | 'VM' | 'VMwareVM': Type of workload this item represents.
### AzureFileshareProtectedItem
#### Properties
* **extendedInfo**: [AzureFileshareProtectedItemExtendedInfo](#azurefileshareprotecteditemextendedinfo): Additional information about Azure File Share backup item.
* **friendlyName**: string: Friendly name of the fileshare represented by this backup item.
* **kpisHealths**: [AzureFileshareProtectedItemKpisHealths](#azurefileshareprotecteditemkpishealths): Health details of different KPIs
* **lastBackupStatus**: string: Last backup operation status. Possible values: Healthy, Unhealthy.
* **lastBackupTime**: string: Timestamp of the last backup operation on this backup item.
* **protectedItemType**: 'AzureFileShareProtectedItem' (Required): backup item type.
* **protectionState**: 'IRPending' | 'Invalid' | 'Protected' | 'ProtectionError' | 'ProtectionPaused' | 'ProtectionStopped': Backup state of this backup item.
* **protectionStatus**: string: Backup status of this backup item.

### AzureVmWorkloadSAPAseDatabaseProtectedItem
#### Properties
* **protectedItemType**: 'AzureVmWorkloadSAPAseDatabase' (Required): backup item type.

### AzureVmWorkloadSAPHanaDatabaseProtectedItem
#### Properties
* **protectedItemType**: 'AzureVmWorkloadSAPHanaDatabase' (Required): backup item type.

### AzureVmWorkloadSQLDatabaseProtectedItem
#### Properties
* **protectedItemType**: 'AzureVmWorkloadSQLDatabase' (Required): backup item type.

### DPMProtectedItem
#### Properties
* **backupEngineName**: string: Backup Management server protecting this backup item
* **extendedInfo**: [DPMProtectedItemExtendedInfo](#dpmprotecteditemextendedinfo): Additional information of DPM Protected item.
* **friendlyName**: string: Friendly name of the managed item
* **protectedItemType**: 'DPMProtectedItem' (Required): backup item type.
* **protectionState**: 'IRPending' | 'Invalid' | 'Protected' | 'ProtectionError' | 'ProtectionPaused' | 'ProtectionStopped': Backup state of the backed up item.

### GenericProtectedItem
#### Properties
* **fabricName**: string: Name of this backup item's fabric.
* **friendlyName**: string: Friendly name of the container.
* **policyState**: string: Indicates consistency of policy object and policy applied to this backup item.
* **protectedItemId**: int: Data Plane Service ID of the protected item.
* **protectedItemType**: 'GenericProtectedItem' (Required): backup item type.
* **protectionState**: 'IRPending' | 'Invalid' | 'Protected' | 'ProtectionError' | 'ProtectionPaused' | 'ProtectionStopped': Backup state of this backup item.
* **sourceAssociations**: [GenericProtectedItemSourceAssociations](#genericprotecteditemsourceassociations): Loosely coupled (type, value) associations (example - parent of a protected item)

### MabFileFolderProtectedItem
#### Properties
* **computerName**: string: Name of the computer associated with this backup item.
* **deferredDeleteSyncTimeInUTC**: int: Sync time for deferred deletion in UTC
* **extendedInfo**: [MabFileFolderProtectedItemExtendedInfo](#mabfilefolderprotecteditemextendedinfo): Additional information on the backed up item.
* **friendlyName**: string: Friendly name of this backup item.
* **lastBackupStatus**: string: Status of last backup operation.
* **lastBackupTime**: string: Timestamp of the last backup operation on this backup item.
* **protectedItemType**: 'MabFileFolderProtectedItem' (Required): backup item type.
* **protectionState**: string: Protected, ProtectionStopped, IRPending or ProtectionError

### AzureIaaSClassicComputeVMProtectedItem
#### Properties
* **protectedItemType**: 'Microsoft.ClassicCompute/virtualMachines' (Required): backup item type.

### AzureIaaSComputeVMProtectedItem
#### Properties
* **protectedItemType**: 'Microsoft.Compute/virtualMachines' (Required): backup item type.

### AzureSqlProtectedItem
#### Properties
* **extendedInfo**: [AzureSqlProtectedItemExtendedInfo](#azuresqlprotecteditemextendedinfo): Additional information on Azure Sql specific protected item.
* **protectedItemDataId**: string: Internal ID of a backup item. Used by Azure SQL Backup engine to contact Recovery Services.
* **protectedItemType**: 'Microsoft.Sql/servers/databases' (Required): backup item type.
* **protectionState**: 'IRPending' | 'Invalid' | 'Protected' | 'ProtectionError' | 'ProtectionPaused' | 'ProtectionStopped': Backup state of the backed up item.


## AzureFileshareProtectedItemExtendedInfo
### Properties
* **oldestRecoveryPoint**: string: The oldest backup copy available for this item in the service.
* **policyState**: string: Indicates consistency of policy object and policy applied to this backup item.
* **recoveryPointCount**: int: Number of available backup copies associated with this backup item.
* **resourceState**: string (ReadOnly): Indicates the state of this resource. Possible values are from enum ResourceState {Invalid, Active, SoftDeleted, Deleted}
* **resourceStateSyncTime**: string (ReadOnly): The resource state sync time for this backup item.

## AzureFileshareProtectedItemKpisHealths
### Properties
### Additional Properties
* **Additional Properties Type**: [KPIResourceHealthDetails](#kpiresourcehealthdetails)

## KPIResourceHealthDetails
### Properties
* **resourceHealthDetails**: [ResourceHealthDetails](#resourcehealthdetails)[]: Resource Health Status
* **resourceHealthStatus**: 'Healthy' | 'Invalid' | 'PersistentDegraded' | 'PersistentUnhealthy' | 'TransientDegraded' | 'TransientUnhealthy': Resource Health Status

## ResourceHealthDetails
### Properties
* **code**: int (ReadOnly): Health Code
* **message**: string (ReadOnly): Health Message
* **recommendations**: string[] (ReadOnly): Health Recommended Actions
* **title**: string (ReadOnly): Health Title

## DPMProtectedItemExtendedInfo
### Properties
* **diskStorageUsedInBytes**: string: Used Disk storage in bytes.
* **isCollocated**: bool: To check if backup item is collocated.
* **isPresentOnCloud**: bool: To check if backup item is cloud protected.
* **lastBackupStatus**: string: Last backup status information on backup item.
* **lastRefreshedAt**: string: Last refresh time on backup item.
* **oldestRecoveryPoint**: string: Oldest cloud recovery point time.
* **onPremiseLatestRecoveryPoint**: string: latest disk recovery point time.
* **onPremiseOldestRecoveryPoint**: string: Oldest disk recovery point time.
* **onPremiseRecoveryPointCount**: int: disk recovery point count.
* **protectableObjectLoadPath**: [DPMProtectedItemExtendedInfoProtectableObjectLoadPath](#dpmprotecteditemextendedinfoprotectableobjectloadpath): Attribute to provide information on various DBs.
* **protected**: bool: To check if backup item is disk protected.
* **protectionGroupName**: string: Protection group name of the backup item.
* **recoveryPointCount**: int: cloud recovery point count.
* **totalDiskStorageSizeInBytes**: string: total Disk storage in bytes.

## DPMProtectedItemExtendedInfoProtectableObjectLoadPath
### Properties
### Additional Properties
* **Additional Properties Type**: string

## GenericProtectedItemSourceAssociations
### Properties
### Additional Properties
* **Additional Properties Type**: string

## MabFileFolderProtectedItemExtendedInfo
### Properties
* **lastRefreshedAt**: string: Last time when the agent data synced to service.
* **oldestRecoveryPoint**: string: The oldest backup copy available.
* **recoveryPointCount**: int: Number of backup copies associated with the backup item.

## AzureSqlProtectedItemExtendedInfo
### Properties
* **oldestRecoveryPoint**: string: The oldest backup copy available for this item in the service.
* **policyState**: string: State of the backup policy associated with this backup item.
* **recoveryPointCount**: int: Number of available backup copies associated with this backup item.

## ResourceTags
### Properties
### Additional Properties
* **Additional Properties Type**: string

## ProtectionPolicy
* **Discriminator**: backupManagementType

### Base Properties
* **protectedItemsCount**: int: Number of items associated with this policy.
* **resourceGuardOperationRequests**: string[]: ResourceGuard Operation Requests
### AzureIaaSVMProtectionPolicy
#### Properties
* **backupManagementType**: 'AzureIaasVM' (Required): This property will be used as the discriminator for deciding the specific types in the polymorphic chain of types.
* **instantRPDetails**: [InstantRPAdditionalDetails](#instantrpadditionaldetails)
* **instantRpRetentionRangeInDays**: int: Instant RP retention policy range in days
* **retentionPolicy**: [RetentionPolicy](#retentionpolicy): Base class for retention policy.
* **schedulePolicy**: [SchedulePolicy](#schedulepolicy): Base class for backup schedule.
* **timeZone**: string: TimeZone optional input as string. For example: TimeZone = "Pacific Standard Time".

### AzureSqlProtectionPolicy
#### Properties
* **backupManagementType**: 'AzureSql' (Required): This property will be used as the discriminator for deciding the specific types in the polymorphic chain of types.
* **retentionPolicy**: [RetentionPolicy](#retentionpolicy): Base class for retention policy.

### AzureFileShareProtectionPolicy
#### Properties
* **backupManagementType**: 'AzureStorage' (Required): This property will be used as the discriminator for deciding the specific types in the polymorphic chain of types.
* **retentionPolicy**: [RetentionPolicy](#retentionpolicy): Base class for retention policy.
* **schedulePolicy**: [SchedulePolicy](#schedulepolicy): Base class for backup schedule.
* **timeZone**: string: TimeZone optional input as string. For example: TimeZone = "Pacific Standard Time".
* **workLoadType**: 'AzureFileShare' | 'AzureSqlDb' | 'Client' | 'Exchange' | 'FileFolder' | 'GenericDataSource' | 'Invalid' | 'SAPAseDatabase' | 'SAPHanaDatabase' | 'SQLDB' | 'SQLDataBase' | 'Sharepoint' | 'SystemState' | 'VM' | 'VMwareVM': Type of workload for the backup management

### AzureVmWorkloadProtectionPolicy
#### Properties
* **backupManagementType**: 'AzureWorkload' (Required): This property will be used as the discriminator for deciding the specific types in the polymorphic chain of types.
* **makePolicyConsistent**: bool: Fix the policy inconsistency
* **settings**: [Settings](#settings): Common settings field for backup management
* **subProtectionPolicy**: [SubProtectionPolicy](#subprotectionpolicy)[]: List of sub-protection policies which includes schedule and retention
* **workLoadType**: 'AzureFileShare' | 'AzureSqlDb' | 'Client' | 'Exchange' | 'FileFolder' | 'GenericDataSource' | 'Invalid' | 'SAPAseDatabase' | 'SAPHanaDatabase' | 'SQLDB' | 'SQLDataBase' | 'Sharepoint' | 'SystemState' | 'VM' | 'VMwareVM': Type of workload for the backup management

### GenericProtectionPolicy
#### Properties
* **backupManagementType**: 'GenericProtectionPolicy' (Required): This property will be used as the discriminator for deciding the specific types in the polymorphic chain of types.
* **fabricName**: string: Name of this policy's fabric.
* **subProtectionPolicy**: [SubProtectionPolicy](#subprotectionpolicy)[]: List of sub-protection policies which includes schedule and retention
* **timeZone**: string: TimeZone optional input as string. For example: TimeZone = "Pacific Standard Time".

### MabProtectionPolicy
#### Properties
* **backupManagementType**: 'MAB' (Required): This property will be used as the discriminator for deciding the specific types in the polymorphic chain of types.
* **retentionPolicy**: [RetentionPolicy](#retentionpolicy): Base class for retention policy.
* **schedulePolicy**: [SchedulePolicy](#schedulepolicy): Base class for backup schedule.


## InstantRPAdditionalDetails
### Properties
* **azureBackupRGNamePrefix**: string
* **azureBackupRGNameSuffix**: string

## RetentionPolicy
* **Discriminator**: retentionPolicyType

### Base Properties
### LongTermRetentionPolicy
#### Properties
* **dailySchedule**: [DailyRetentionSchedule](#dailyretentionschedule): Daily retention schedule.
* **monthlySchedule**: [MonthlyRetentionSchedule](#monthlyretentionschedule): Monthly retention schedule.
* **retentionPolicyType**: 'LongTermRetentionPolicy' (Required): This property will be used as the discriminator for deciding the specific types in the polymorphic chain of types.
* **weeklySchedule**: [WeeklyRetentionSchedule](#weeklyretentionschedule): Weekly retention schedule.
* **yearlySchedule**: [YearlyRetentionSchedule](#yearlyretentionschedule): Yearly retention schedule.

### SimpleRetentionPolicy
#### Properties
* **retentionDuration**: [RetentionDuration](#retentionduration): Retention duration.
* **retentionPolicyType**: 'SimpleRetentionPolicy' (Required): This property will be used as the discriminator for deciding the specific types in the polymorphic chain of types.


## DailyRetentionSchedule
### Properties
* **retentionDuration**: [RetentionDuration](#retentionduration): Retention duration.
* **retentionTimes**: string[]: Retention times of retention policy.

## RetentionDuration
### Properties
* **count**: int: Count of duration types. Retention duration is obtained by the counting the duration type Count times.
For example, when Count = 3 and DurationType = Weeks, retention duration will be three weeks.
* **durationType**: 'Days' | 'Invalid' | 'Months' | 'Weeks' | 'Years': Retention duration type of retention policy.

## MonthlyRetentionSchedule
### Properties
* **retentionDuration**: [RetentionDuration](#retentionduration): Retention duration.
* **retentionScheduleDaily**: [DailyRetentionFormat](#dailyretentionformat): Daily retention format.
* **retentionScheduleFormatType**: 'Daily' | 'Invalid' | 'Weekly': Retention schedule format type for monthly retention policy.
* **retentionScheduleWeekly**: [WeeklyRetentionFormat](#weeklyretentionformat): Weekly retention format.
* **retentionTimes**: string[]: Retention times of retention policy.

## DailyRetentionFormat
### Properties
* **daysOfTheMonth**: [Day](#day)[]: List of days of the month.

## Day
### Properties
* **date**: int: Date of the month
* **isLast**: bool: Whether Date is last date of month

## WeeklyRetentionFormat
### Properties
* **daysOfTheWeek**: 'Friday' | 'Monday' | 'Saturday' | 'Sunday' | 'Thursday' | 'Tuesday' | 'Wednesday'[]: List of days of the week.
* **weeksOfTheMonth**: 'First' | 'Fourth' | 'Invalid' | 'Last' | 'Second' | 'Third'[]: List of weeks of month.

## WeeklyRetentionSchedule
### Properties
* **daysOfTheWeek**: 'Friday' | 'Monday' | 'Saturday' | 'Sunday' | 'Thursday' | 'Tuesday' | 'Wednesday'[]: List of days of week for weekly retention policy.
* **retentionDuration**: [RetentionDuration](#retentionduration): Retention duration.
* **retentionTimes**: string[]: Retention times of retention policy.

## YearlyRetentionSchedule
### Properties
* **monthsOfYear**: 'April' | 'August' | 'December' | 'February' | 'Invalid' | 'January' | 'July' | 'June' | 'March' | 'May' | 'November' | 'October' | 'September'[]: List of months of year of yearly retention policy.
* **retentionDuration**: [RetentionDuration](#retentionduration): Retention duration.
* **retentionScheduleDaily**: [DailyRetentionFormat](#dailyretentionformat): Daily retention format.
* **retentionScheduleFormatType**: 'Daily' | 'Invalid' | 'Weekly': Retention schedule format type for monthly retention policy.
* **retentionScheduleWeekly**: [WeeklyRetentionFormat](#weeklyretentionformat): Weekly retention format.
* **retentionTimes**: string[]: Retention times of retention policy.

## SchedulePolicy
* **Discriminator**: schedulePolicyType

### Base Properties
### LogSchedulePolicy
#### Properties
* **scheduleFrequencyInMins**: int: Frequency of the log schedule operation of this policy in minutes.
* **schedulePolicyType**: 'LogSchedulePolicy' (Required): This property will be used as the discriminator for deciding the specific types in the polymorphic chain of types.

### LongTermSchedulePolicy
#### Properties
* **schedulePolicyType**: 'LongTermSchedulePolicy' (Required): This property will be used as the discriminator for deciding the specific types in the polymorphic chain of types.

### SimpleSchedulePolicy
#### Properties
* **hourlySchedule**: [HourlySchedule](#hourlyschedule)
* **schedulePolicyType**: 'SimpleSchedulePolicy' (Required): This property will be used as the discriminator for deciding the specific types in the polymorphic chain of types.
* **scheduleRunDays**: 'Friday' | 'Monday' | 'Saturday' | 'Sunday' | 'Thursday' | 'Tuesday' | 'Wednesday'[]: List of days of week this schedule has to be run.
* **scheduleRunFrequency**: 'Daily' | 'Hourly' | 'Invalid' | 'Weekly': Frequency of the schedule operation of this policy.
* **scheduleRunTimes**: string[]: List of times of day this schedule has to be run.
* **scheduleWeeklyFrequency**: int: At every number weeks this schedule has to be run.


## HourlySchedule
### Properties
* **interval**: int: Interval at which backup needs to be triggered. For hourly the value
 can be 4/6/8/12
* **scheduleWindowDuration**: int: To specify duration of the backup window
* **scheduleWindowStartTime**: string: To specify start time of the backup window

## Settings
### Properties
* **isCompression**: bool: Workload compression flag. This has been added so that 'isSqlCompression'
will be deprecated once clients upgrade to consider this flag.
* **issqlcompression**: bool: SQL compression flag
* **timeZone**: string: TimeZone optional input as string. For example: TimeZone = "Pacific Standard Time".

## SubProtectionPolicy
### Properties
* **policyType**: 'CopyOnlyFull' | 'Differential' | 'Full' | 'Incremental' | 'Invalid' | 'Log': Type of backup policy type
* **retentionPolicy**: [RetentionPolicy](#retentionpolicy): Base class for retention policy.
* **schedulePolicy**: [SchedulePolicy](#schedulepolicy): Base class for backup schedule.

## ResourceTags
### Properties
### Additional Properties
* **Additional Properties Type**: string

## ResourceGuardProxyBase
### Properties
* **description**: string (ReadOnly)
* **lastUpdatedTime**: string (ReadOnly)
* **resourceGuardOperationDetails**: [ResourceGuardOperationDetail](#resourceguardoperationdetail)[] (ReadOnly): Array of ResourceGuardOperationDetail
* **resourceGuardResourceId**: string (ReadOnly)

## ResourceGuardOperationDetail
### Properties
* **defaultResourceRequest**: string (ReadOnly)
* **vaultCriticalOperation**: string (ReadOnly)

## ResourceTags
### Properties
### Additional Properties
* **Additional Properties Type**: string

## BackupResourceConfig
### Properties
* **crossRegionRestoreFlag**: bool: Opt in details of Cross Region Restore feature.
* **dedupState**: 'Disabled' | 'Enabled' | 'Invalid': Vault Dedup state
* **storageModelType**: 'GeoRedundant' | 'Invalid' | 'LocallyRedundant' | 'ReadAccessGeoZoneRedundant' | 'ZoneRedundant': Storage type
* **storageType**: 'GeoRedundant' | 'Invalid' | 'LocallyRedundant' | 'ReadAccessGeoZoneRedundant' | 'ZoneRedundant': Storage type
* **storageTypeState**: 'Invalid' | 'Locked' | 'Unlocked': Locked or Unlocked. Once a machine is registered against a resource, the storageTypeState is always Locked.
* **xcoolState**: 'Disabled' | 'Enabled' | 'Invalid': Vault x-cool state

## ResourceTags
### Properties
### Additional Properties
* **Additional Properties Type**: string

## PrivateEndpointConnection
### Properties
* **privateEndpoint**: [PrivateEndpoint](#privateendpoint): The Private Endpoint network resource that is linked to the Private Endpoint connection
* **privateLinkServiceConnectionState**: [PrivateLinkServiceConnectionState](#privatelinkserviceconnectionstate): Private Link Service Connection State
* **provisioningState**: 'Deleting' | 'Failed' | 'Pending' | 'Succeeded': Gets or sets provisioning state of the private endpoint connection

## PrivateEndpoint
### Properties
* **id**: string: Gets or sets id

## PrivateLinkServiceConnectionState
### Properties
* **actionRequired**: string: Gets or sets actions required
* **description**: string: Gets or sets description
* **status**: 'Approved' | 'Disconnected' | 'Pending' | 'Rejected': Gets or sets the status

## ResourceTags
### Properties
### Additional Properties
* **Additional Properties Type**: string

