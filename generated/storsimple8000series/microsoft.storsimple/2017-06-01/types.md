# Microsoft.StorSimple @ 2017-06-01

## Resource Microsoft.StorSimple/managers@2017-06-01
* **Valid Scope(s)**: ResourceGroup
### Properties
* **apiVersion**: '2017-06-01' (ReadOnly, DeployTimeConstant): The resource api version
* **etag**: string: The etag of the manager.
* **id**: string (ReadOnly, DeployTimeConstant): The resource id
* **location**: string (Required): The geo location of the resource.
* **name**: string (Required, DeployTimeConstant): The resource name
* **properties**: [ManagerProperties](#managerproperties): The properties of the StorSimple Manager.
* **tags**: [ResourceTags](#resourcetags): The tags attached to the resource.
* **type**: 'Microsoft.StorSimple/managers' (ReadOnly, DeployTimeConstant): The resource type

## Resource Microsoft.StorSimple/managers/accessControlRecords@2017-06-01
* **Valid Scope(s)**: ResourceGroup
### Properties
* **apiVersion**: '2017-06-01' (ReadOnly, DeployTimeConstant): The resource api version
* **id**: string (ReadOnly, DeployTimeConstant): The resource id
* **kind**: 'Series8000': The Kind of the object. Currently only Series8000 is supported
* **name**: string (Required, DeployTimeConstant): The resource name
* **properties**: [AccessControlRecordProperties](#accesscontrolrecordproperties) (Required): The properties of access control record.
* **type**: 'Microsoft.StorSimple/managers/accessControlRecords' (ReadOnly, DeployTimeConstant): The resource type

## Resource Microsoft.StorSimple/managers/bandwidthSettings@2017-06-01
* **Valid Scope(s)**: ResourceGroup
### Properties
* **apiVersion**: '2017-06-01' (ReadOnly, DeployTimeConstant): The resource api version
* **id**: string (ReadOnly, DeployTimeConstant): The resource id
* **kind**: 'Series8000': The Kind of the object. Currently only Series8000 is supported
* **name**: string (Required, DeployTimeConstant): The resource name
* **properties**: [BandwidthRateSettingProperties](#bandwidthratesettingproperties) (Required): The properties of the bandwidth setting.
* **type**: 'Microsoft.StorSimple/managers/bandwidthSettings' (ReadOnly, DeployTimeConstant): The resource type

## Resource Microsoft.StorSimple/managers/devices/alertSettings@2017-06-01
* **Valid Scope(s)**: ResourceGroup
### Properties
* **apiVersion**: '2017-06-01' (ReadOnly, DeployTimeConstant): The resource api version
* **id**: string (ReadOnly, DeployTimeConstant): The resource id
* **kind**: 'Series8000': The Kind of the object. Currently only Series8000 is supported
* **name**: 'default' (Required, DeployTimeConstant): The resource name
* **properties**: [AlertNotificationProperties](#alertnotificationproperties) (Required): The properties of the alert notification settings.
* **type**: 'Microsoft.StorSimple/managers/devices/alertSettings' (ReadOnly, DeployTimeConstant): The resource type

## Resource Microsoft.StorSimple/managers/devices/backupPolicies@2017-06-01
* **Valid Scope(s)**: ResourceGroup
### Properties
* **apiVersion**: '2017-06-01' (ReadOnly, DeployTimeConstant): The resource api version
* **id**: string (ReadOnly, DeployTimeConstant): The resource id
* **kind**: 'Series8000': The Kind of the object. Currently only Series8000 is supported
* **name**: string (Required, DeployTimeConstant): The resource name
* **properties**: [BackupPolicyProperties](#backuppolicyproperties) (Required): The properties of the backup policy.
* **type**: 'Microsoft.StorSimple/managers/devices/backupPolicies' (ReadOnly, DeployTimeConstant): The resource type

## Resource Microsoft.StorSimple/managers/devices/backupPolicies/schedules@2017-06-01
* **Valid Scope(s)**: ResourceGroup
### Properties
* **apiVersion**: '2017-06-01' (ReadOnly, DeployTimeConstant): The resource api version
* **id**: string (ReadOnly, DeployTimeConstant): The resource id
* **kind**: 'Series8000': The Kind of the object. Currently only Series8000 is supported
* **name**: string (Required, DeployTimeConstant): The resource name
* **properties**: [BackupScheduleProperties](#backupscheduleproperties) (Required): The properties of the backup schedule.
* **type**: 'Microsoft.StorSimple/managers/devices/backupPolicies/schedules' (ReadOnly, DeployTimeConstant): The resource type

## Resource Microsoft.StorSimple/managers/devices/timeSettings@2017-06-01
* **Valid Scope(s)**: ResourceGroup
### Properties
* **apiVersion**: '2017-06-01' (ReadOnly, DeployTimeConstant): The resource api version
* **id**: string (ReadOnly, DeployTimeConstant): The resource id
* **kind**: 'Series8000': The Kind of the object. Currently only Series8000 is supported
* **name**: 'default' (Required, DeployTimeConstant): The resource name
* **properties**: [TimeSettingsProperties](#timesettingsproperties) (Required): The properties of time settings of a device.
* **type**: 'Microsoft.StorSimple/managers/devices/timeSettings' (ReadOnly, DeployTimeConstant): The resource type

## Resource Microsoft.StorSimple/managers/devices/volumeContainers@2017-06-01
* **Valid Scope(s)**: ResourceGroup
### Properties
* **apiVersion**: '2017-06-01' (ReadOnly, DeployTimeConstant): The resource api version
* **id**: string (ReadOnly, DeployTimeConstant): The resource id
* **kind**: 'Series8000': The Kind of the object. Currently only Series8000 is supported
* **name**: string (Required, DeployTimeConstant): The resource name
* **properties**: [VolumeContainerProperties](#volumecontainerproperties) (Required): The properties of volume container.
* **type**: 'Microsoft.StorSimple/managers/devices/volumeContainers' (ReadOnly, DeployTimeConstant): The resource type

## Resource Microsoft.StorSimple/managers/devices/volumeContainers/volumes@2017-06-01
* **Valid Scope(s)**: ResourceGroup
### Properties
* **apiVersion**: '2017-06-01' (ReadOnly, DeployTimeConstant): The resource api version
* **id**: string (ReadOnly, DeployTimeConstant): The resource id
* **kind**: 'Series8000': The Kind of the object. Currently only Series8000 is supported
* **name**: string (Required, DeployTimeConstant): The resource name
* **properties**: [VolumeProperties](#volumeproperties) (Required): The properties of volume.
* **type**: 'Microsoft.StorSimple/managers/devices/volumeContainers/volumes' (ReadOnly, DeployTimeConstant): The resource type

## Resource Microsoft.StorSimple/managers/extendedInformation@2017-06-01
* **Valid Scope(s)**: ResourceGroup
### Properties
* **apiVersion**: '2017-06-01' (ReadOnly, DeployTimeConstant): The resource api version
* **etag**: string: The etag of the resource.
* **id**: string (ReadOnly, DeployTimeConstant): The resource id
* **kind**: 'Series8000': The Kind of the object. Currently only Series8000 is supported
* **name**: 'vaultExtendedInfo' (Required, DeployTimeConstant): The resource name
* **properties**: [ManagerExtendedInfoProperties](#managerextendedinfoproperties): The properties of the manager extended info.
* **type**: 'Microsoft.StorSimple/managers/extendedInformation' (ReadOnly, DeployTimeConstant): The resource type

## Resource Microsoft.StorSimple/managers/storageAccountCredentials@2017-06-01
* **Valid Scope(s)**: ResourceGroup
### Properties
* **apiVersion**: '2017-06-01' (ReadOnly, DeployTimeConstant): The resource api version
* **id**: string (ReadOnly, DeployTimeConstant): The resource id
* **kind**: 'Series8000': The Kind of the object. Currently only Series8000 is supported
* **name**: string (Required, DeployTimeConstant): The resource name
* **properties**: [StorageAccountCredentialProperties](#storageaccountcredentialproperties) (Required): The storage account credential properties.
* **type**: 'Microsoft.StorSimple/managers/storageAccountCredentials' (ReadOnly, DeployTimeConstant): The resource type

## Function listActivationKey (Microsoft.StorSimple/managers@2017-06-01)
* **Resource**: Microsoft.StorSimple/managers
* **ApiVersion**: 2017-06-01
* **Output**: [Key](#key)

## Function listFailoverSets (Microsoft.StorSimple/managers/devices@2017-06-01)
* **Resource**: Microsoft.StorSimple/managers/devices
* **ApiVersion**: 2017-06-01
* **Output**: [FailoverSetsList](#failoversetslist)

## Function listFailoverTargets (Microsoft.StorSimple/managers/devices@2017-06-01)
* **Resource**: Microsoft.StorSimple/managers/devices
* **ApiVersion**: 2017-06-01
* **Input**: [ListFailoverTargetsRequest](#listfailovertargetsrequest)
* **Output**: [FailoverTargetsList](#failovertargetslist)

## Function listPublicEncryptionKey (Microsoft.StorSimple/managers@2017-06-01)
* **Resource**: Microsoft.StorSimple/managers
* **ApiVersion**: 2017-06-01
* **Output**: [SymmetricEncryptedSecret](#symmetricencryptedsecret)

## ManagerProperties
### Properties
* **cisIntrinsicSettings**: [ManagerIntrinsicSettings](#managerintrinsicsettings): Intrinsic settings which refers to the type of the StorSimple Manager.
* **provisioningState**: string: Specifies the state of the resource as it is getting provisioned. Value of "Succeeded" means the Manager was successfully created.
* **sku**: [ManagerSku](#managersku): The Sku.

## ManagerIntrinsicSettings
### Properties
* **type**: 'GardaV1' | 'HelsinkiV1' (Required): The type of StorSimple Manager.

## ManagerSku
### Properties
* **name**: 'Standard' (Required): Refers to the sku name which should be "Standard"

## ResourceTags
### Properties
### Additional Properties
* **Additional Properties Type**: string

## AccessControlRecordProperties
### Properties
* **initiatorName**: string (Required): The iSCSI initiator name (IQN).
* **volumeCount**: int (ReadOnly): The number of volumes using the access control record.

## BandwidthRateSettingProperties
### Properties
* **schedules**: [BandwidthSchedule](#bandwidthschedule)[] (Required): The schedules.
* **volumeCount**: int (ReadOnly): The number of volumes that uses the bandwidth setting.

## BandwidthSchedule
### Properties
* **days**: 'Friday' | 'Monday' | 'Saturday' | 'Sunday' | 'Thursday' | 'Tuesday' | 'Wednesday'[] (Required): The days of the week when this schedule is applicable.
* **rateInMbps**: int (Required): The rate in Mbps.
* **start**: [Time](#time) (Required): The time.
* **stop**: [Time](#time) (Required): The time.

## Time
### Properties
* **hours**: int (Required): The hour.
* **minutes**: int (Required): The minute.
* **seconds**: int (Required): The second.

## AlertNotificationProperties
### Properties
* **additionalRecipientEmailList**: string[]: The alert notification email list.
* **alertNotificationCulture**: string: The alert notification culture.
* **emailNotification**: 'Disabled' | 'Enabled' (Required): Indicates whether email notification enabled or not.
* **notificationToServiceOwners**: 'Disabled' | 'Enabled': Indicates whether email notification enabled or not.

## BackupPolicyProperties
### Properties
* **backupPolicyCreationType**: 'BySSM' | 'BySaaS' (ReadOnly): The backup policy creation type. Indicates whether this was created through SaaS or through StorSimple Snapshot Manager.
* **lastBackupTime**: string (ReadOnly): The time of the last backup for the backup policy.
* **nextBackupTime**: string (ReadOnly): The time of the next backup for the backup policy.
* **scheduledBackupStatus**: 'Disabled' | 'Enabled' (ReadOnly): Indicates whether at least one of the schedules in the backup policy is active or not.
* **schedulesCount**: int (ReadOnly): The count of schedules the backup policy contains.
* **ssmHostName**: string (ReadOnly): If the backup policy was created by StorSimple Snapshot Manager, then this field indicates the hostname of the StorSimple Snapshot Manager.
* **volumeIds**: string[] (Required): The path IDs of the volumes which are part of the backup policy.

## BackupScheduleProperties
### Properties
* **backupType**: 'CloudSnapshot' | 'LocalSnapshot' (Required): The type of the backup.
* **lastSuccessfulRun**: string (ReadOnly): The last successful backup run which was triggered for the schedule.
* **retentionCount**: int (Required): The number of backups to be retained.
* **scheduleRecurrence**: [ScheduleRecurrence](#schedulerecurrence) (Required): The schedule recurrence.
* **scheduleStatus**: 'Disabled' | 'Enabled' (Required): The schedule status.
* **startTime**: string (Required): The start time of the schedule.

## ScheduleRecurrence
### Properties
* **recurrenceType**: 'Daily' | 'Hourly' | 'Minutes' | 'Weekly' (Required): The recurrence type.
* **recurrenceValue**: int (Required): The recurrence value.
* **weeklyDaysList**: 'Friday' | 'Monday' | 'Saturday' | 'Sunday' | 'Thursday' | 'Tuesday' | 'Wednesday'[]: The week days list. Applicable only for schedules of recurrence type 'weekly'.

## TimeSettingsProperties
### Properties
* **primaryTimeServer**: string: The primary Network Time Protocol (NTP) server name, like 'time.windows.com'.
* **secondaryTimeServer**: string[]: The secondary Network Time Protocol (NTP) server name, like 'time.contoso.com'. It's optional.
* **timeZone**: string (Required): The timezone of device, like '(UTC -06:00) Central America'

## VolumeContainerProperties
### Properties
* **bandWidthRateInMbps**: int: The bandwidth-rate set on the volume container.
* **bandwidthSettingId**: string: The ID of the bandwidth setting associated with the volume container.
* **encryptionKey**: [AsymmetricEncryptedSecret](#asymmetricencryptedsecret): Represent the secrets intended for encryption with asymmetric key pair.
* **encryptionStatus**: 'Disabled' | 'Enabled' (ReadOnly): The encryption status to indicates if encryption is enabled or not.
* **ownerShipStatus**: 'NotOwned' | 'Owned' (ReadOnly): The owner ship status of the volume container. Only when the status is "NotOwned", the delete operation on the volume container is permitted.
* **storageAccountCredentialId**: string (Required): The path ID of storage account associated with the volume container.
* **totalCloudStorageUsageInBytes**: int (ReadOnly): The total cloud storage for the volume container.
* **volumeCount**: int (ReadOnly): The number of volumes in the volume Container.

## AsymmetricEncryptedSecret
### Properties
* **encryptionAlgorithm**: 'AES256' | 'None' | 'RSAES_PKCS1_v_1_5' (Required): The algorithm used to encrypt "Value".
* **encryptionCertThumbprint**: string: Thumbprint certificate that was used to encrypt "Value". If the value in unencrypted, it will be null.
* **value**: string (Required): The value of the secret.

## VolumeProperties
### Properties
* **accessControlRecordIds**: string[] (Required): The IDs of the access control records, associated with the volume.
* **backupPolicyIds**: string[] (ReadOnly): The IDs of the backup policies, in which this volume is part of.
* **backupStatus**: 'Disabled' | 'Enabled' (ReadOnly): The backup status of the volume.
* **monitoringStatus**: 'Disabled' | 'Enabled' (Required): The monitoring status of the volume.
* **operationStatus**: 'Deleting' | 'None' | 'Restoring' | 'Updating' (ReadOnly): The operation status on the volume.
* **sizeInBytes**: int (Required): The size of the volume in bytes.
* **volumeContainerId**: string (ReadOnly): The ID of the volume container, in which this volume is created.
* **volumeStatus**: 'Offline' | 'Online' (Required): The volume status.
* **volumeType**: 'Archival' | 'LocallyPinned' | 'Tiered' (Required): The volume type.

## ManagerExtendedInfoProperties
### Properties
* **algorithm**: string (Required): Represents the encryption algorithm used to encrypt the keys. None - if Key is saved in plain text format. Algorithm name - if key is encrypted
* **encryptionKey**: string: Represents the CEK of the resource.
* **encryptionKeyThumbprint**: string: Represents the Cert thumbprint that was used to encrypt the CEK.
* **integrityKey**: string (Required): Represents the CIK of the resource.
* **portalCertificateThumbprint**: string: Represents the portal thumbprint which can be used optionally to encrypt the entire data before storing it.
* **version**: string: The version of the extended info being persisted.

## StorageAccountCredentialProperties
### Properties
* **accessKey**: [AsymmetricEncryptedSecret](#asymmetricencryptedsecret): Represent the secrets intended for encryption with asymmetric key pair.
* **endPoint**: string (Required): The storage endpoint
* **sslStatus**: 'Disabled' | 'Enabled' (Required): Signifies whether SSL needs to be enabled or not.
* **volumesCount**: int (ReadOnly): The count of volumes using this storage account credential.

## Key
### Properties
* **activationKey**: string (ReadOnly): The activation key for the device.

## FailoverSetsList
### Properties
* **value**: [FailoverSet](#failoverset)[] (ReadOnly): The list of failover sets.

## FailoverSet
### Properties
* **eligibilityResult**: [FailoverSetEligibilityResult](#failoverseteligibilityresult) (ReadOnly): The eligibility result of failover set, for failover.
* **volumeContainers**: [VolumeContainerFailoverMetadata](#volumecontainerfailovermetadata)[] (ReadOnly): The list of meta data of volume containers, which are part of the failover set.

## FailoverSetEligibilityResult
### Properties
* **errorMessage**: string (ReadOnly): The error message, if the failover set is not eligible for failover.
* **isEligibleForFailover**: bool (ReadOnly): Represents if this failover set is eligible for failover or not.

## VolumeContainerFailoverMetadata
### Properties
* **volumeContainerId**: string (ReadOnly): The path ID of the volume container.
* **volumes**: [VolumeFailoverMetadata](#volumefailovermetadata)[] (ReadOnly): The list of metadata of volumes inside the volume container, which contains valid cloud snapshots.

## VolumeFailoverMetadata
### Properties
* **backupCreatedDate**: string (ReadOnly): The date at which the snapshot was taken.
* **backupElementId**: string (ReadOnly): The path ID of the backup-element for this volume, inside the backup set.
* **backupId**: string (ReadOnly): The path ID of the backup set.
* **backupPolicyId**: string (ReadOnly): The path ID of the backup policy using which the snapshot was taken.
* **sizeInBytes**: int (ReadOnly): The size of the volume in bytes at the time the snapshot was taken.
* **volumeId**: string (ReadOnly): The path ID of the volume.
* **volumeType**: 'Archival' | 'LocallyPinned' | 'Tiered' (ReadOnly): The volume type.

## ListFailoverTargetsRequest
### Properties
* **volumeContainers**: string[] (WriteOnly): The list of path IDs of the volume containers that needs to be failed-over, for which we want to fetch the eligible targets.

## FailoverTargetsList
### Properties
* **value**: [FailoverTarget](#failovertarget)[] (ReadOnly): The list of all the failover targets.

## FailoverTarget
### Properties
* **availableLocalStorageInBytes**: int (ReadOnly): The amount of free local storage available on the device in bytes.
* **availableTieredStorageInBytes**: int (ReadOnly): The amount of free tiered storage available for the device in bytes.
* **dataContainersCount**: int (ReadOnly): The count of data containers on the device.
* **deviceId**: string (ReadOnly): The path ID of the device.
* **deviceLocation**: string (ReadOnly): The geo location (applicable only for cloud appliances) of the device.
* **deviceSoftwareVersion**: string (ReadOnly): The software version of the device.
* **deviceStatus**: 'Creating' | 'Deactivated' | 'Deactivating' | 'Deleted' | 'MaintenanceMode' | 'Offline' | 'Online' | 'Provisioning' | 'ReadyToSetup' | 'RequiresAttention' | 'Unknown' (ReadOnly): The current status of the device.
* **eligibilityResult**: [TargetEligibilityResult](#targeteligibilityresult) (ReadOnly): The eligibility result of device, as a failover target device.
* **friendlyDeviceSoftwareVersion**: string (ReadOnly): The friendly name for the current version of software on the device.
* **modelDescription**: string (ReadOnly): The model number of the device.
* **volumesCount**: int (ReadOnly): The count of volumes on the device.

## TargetEligibilityResult
### Properties
* **eligibilityStatus**: 'Eligible' | 'NotEligible' (ReadOnly): The eligibility status of device, as a failover target device.
* **messages**: [TargetEligibilityErrorMessage](#targeteligibilityerrormessage)[] (ReadOnly): The list of error messages, if a device does not qualify as a failover target device.

## TargetEligibilityErrorMessage
### Properties
* **message**: string (ReadOnly): The localized error message stating the reason why the device is not eligible as a target device.
* **resolution**: string (ReadOnly): The localized resolution message for the error.
* **resultCode**: 'LocalToTieredVolumesConversionWarning' | 'TargetAndSourceCannotBeSameError' | 'TargetInsufficientCapacityError' | 'TargetInsufficientLocalVolumeMemoryError' | 'TargetInsufficientTieredVolumeMemoryError' | 'TargetIsNotOnlineError' | 'TargetSourceIncompatibleVersionError' (ReadOnly): The result code for the error, due to which the device does not qualify as a failover target device.

## SymmetricEncryptedSecret
### Properties
* **encryptionAlgorithm**: 'AES256' | 'None' | 'RSAES_PKCS1_v_1_5' (ReadOnly): The algorithm used to encrypt "Value".
* **value**: string (ReadOnly): The value of the secret itself. If the secret is in plaintext or null then EncryptionAlgorithm will be none.
* **valueCertificateThumbprint**: string (ReadOnly): The thumbprint of the cert that was used to encrypt "Value".

