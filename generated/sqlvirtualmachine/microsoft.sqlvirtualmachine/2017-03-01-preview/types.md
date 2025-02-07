# Microsoft.SqlVirtualMachine @ 2017-03-01-preview

## Resource Microsoft.SqlVirtualMachine/sqlVirtualMachineGroups@2017-03-01-preview
* **Valid Scope(s)**: ResourceGroup
### Properties
* **apiVersion**: '2017-03-01-preview' (ReadOnly, DeployTimeConstant): The resource api version
* **id**: string (ReadOnly, DeployTimeConstant): The resource id
* **location**: string (Required): Resource location.
* **name**: string (Required, DeployTimeConstant): The resource name
* **properties**: [SqlVirtualMachineGroupProperties](#sqlvirtualmachinegroupproperties): The properties of a SQL virtual machine group.
* **tags**: [TrackedResourceTags](#trackedresourcetags): Resource tags.
* **type**: 'Microsoft.SqlVirtualMachine/sqlVirtualMachineGroups' (ReadOnly, DeployTimeConstant): The resource type

## Resource Microsoft.SqlVirtualMachine/sqlVirtualMachineGroups/availabilityGroupListeners@2017-03-01-preview
* **Valid Scope(s)**: ResourceGroup
### Properties
* **apiVersion**: '2017-03-01-preview' (ReadOnly, DeployTimeConstant): The resource api version
* **id**: string (ReadOnly, DeployTimeConstant): The resource id
* **name**: string (Required, DeployTimeConstant): The resource name
* **properties**: [AvailabilityGroupListenerProperties](#availabilitygrouplistenerproperties): The properties of an availability group listener.
* **type**: 'Microsoft.SqlVirtualMachine/sqlVirtualMachineGroups/availabilityGroupListeners' (ReadOnly, DeployTimeConstant): The resource type

## Resource Microsoft.SqlVirtualMachine/sqlVirtualMachines@2017-03-01-preview
* **Valid Scope(s)**: ResourceGroup
### Properties
* **apiVersion**: '2017-03-01-preview' (ReadOnly, DeployTimeConstant): The resource api version
* **id**: string (ReadOnly, DeployTimeConstant): The resource id
* **identity**: [ResourceIdentity](#resourceidentity): Azure Active Directory identity configuration for a resource.
* **location**: string (Required): Resource location.
* **name**: string (Required, DeployTimeConstant): The resource name
* **properties**: [SqlVirtualMachineProperties](#sqlvirtualmachineproperties): The SQL virtual machine properties.
* **tags**: [TrackedResourceTags](#trackedresourcetags): Resource tags.
* **type**: 'Microsoft.SqlVirtualMachine/sqlVirtualMachines' (ReadOnly, DeployTimeConstant): The resource type

## SqlVirtualMachineGroupProperties
### Properties
* **clusterConfiguration**: 'Domainful' (ReadOnly): Cluster type.
* **clusterManagerType**: 'WSFC' (ReadOnly): Type of cluster manager: Windows Server Failover Cluster (WSFC), implied by the scale type of the group and the OS type.
* **provisioningState**: string (ReadOnly): Provisioning state to track the async operation status.
* **scaleType**: 'HA' (ReadOnly): Scale type.
* **sqlImageOffer**: string: SQL image offer. Examples may include SQL2016-WS2016, SQL2017-WS2016.
* **sqlImageSku**: 'Developer' | 'Enterprise': SQL image sku.
* **wsfcDomainProfile**: [WsfcDomainProfile](#wsfcdomainprofile): Active Directory account details to operate Windows Server Failover Cluster.

## WsfcDomainProfile
### Properties
* **clusterBootstrapAccount**: string: Account name used for creating cluster (at minimum needs permissions to 'Create Computer Objects' in domain).
* **clusterOperatorAccount**: string: Account name used for operating cluster i.e. will be part of administrators group on all the participating virtual machines in the cluster.
* **domainFqdn**: string: Fully qualified name of the domain.
* **fileShareWitnessPath**: string: Optional path for fileshare witness.
* **ouPath**: string: Organizational Unit path in which the nodes and cluster will be present.
* **sqlServiceAccount**: string: Account name under which SQL service will run on all participating SQL virtual machines in the cluster.
* **storageAccountPrimaryKey**: string (WriteOnly): Primary key of the witness storage account.
* **storageAccountUrl**: string: Fully qualified ARM resource id of the witness storage account.

## TrackedResourceTags
### Properties
### Additional Properties
* **Additional Properties Type**: string

## AvailabilityGroupListenerProperties
### Properties
* **availabilityGroupName**: string: Name of the availability group.
* **createDefaultAvailabilityGroupIfNotExist**: bool: Create a default availability group if it does not exist.
* **loadBalancerConfigurations**: [LoadBalancerConfiguration](#loadbalancerconfiguration)[]: List of load balancer configurations for an availability group listener.
* **port**: int: Listener port.
* **provisioningState**: string (ReadOnly): Provisioning state to track the async operation status.

## LoadBalancerConfiguration
### Properties
* **loadBalancerResourceId**: string: Resource id of the load balancer.
* **privateIpAddress**: [PrivateIPAddress](#privateipaddress): A private IP address bound to the availability group listener.
* **probePort**: int: Probe port.
* **publicIpAddressResourceId**: string: Resource id of the public IP.
* **sqlVirtualMachineInstances**: string[]: List of the SQL virtual machine instance resource id's that are enrolled into the availability group listener.

## PrivateIPAddress
### Properties
* **ipAddress**: string: Private IP address bound to the availability group listener.
* **subnetResourceId**: string: Subnet used to include private IP.

## ResourceIdentity
### Properties
* **principalId**: string (ReadOnly): The Azure Active Directory principal id.
* **tenantId**: string (ReadOnly): The Azure Active Directory tenant id.
* **type**: 'SystemAssigned': The identity type. Set this to 'SystemAssigned' in order to automatically create and assign an Azure Active Directory principal for the resource.

## SqlVirtualMachineProperties
### Properties
* **autoBackupSettings**: [AutoBackupSettings](#autobackupsettings): Configure backups for databases in your SQL virtual machine.
* **autoPatchingSettings**: [AutoPatchingSettings](#autopatchingsettings): Set a patching window during which Windows and SQL patches will be applied.
* **keyVaultCredentialSettings**: [KeyVaultCredentialSettings](#keyvaultcredentialsettings): Configure your SQL virtual machine to be able to connect to the Azure Key Vault service.
* **provisioningState**: string (ReadOnly): Provisioning state to track the async operation status.
* **serverConfigurationsManagementSettings**: [ServerConfigurationsManagementSettings](#serverconfigurationsmanagementsettings): Set the connectivity, storage and workload settings.
* **sqlImageOffer**: string: SQL image offer. Examples include SQL2016-WS2016, SQL2017-WS2016.
* **sqlImageSku**: 'Developer' | 'Enterprise' | 'Express' | 'Standard' | 'Web': SQL Server edition type.
* **sqlManagement**: 'Full' | 'LightWeight' | 'NoAgent': SQL Server Management type.
* **sqlServerLicenseType**: 'AHUB' | 'DR' | 'PAYG': SQL Server license type.
* **sqlVirtualMachineGroupResourceId**: string: ARM resource id of the SQL virtual machine group this SQL virtual machine is or will be part of.
* **storageConfigurationSettings**: [StorageConfigurationSettings](#storageconfigurationsettings): Storage Configurations for SQL Data, Log and TempDb.
* **virtualMachineResourceId**: string: ARM Resource id of underlying virtual machine created from SQL marketplace image.
* **wsfcDomainCredentials**: [WsfcDomainCredentials](#wsfcdomaincredentials): Domain credentials for setting up Windows Server Failover Cluster for SQL availability group.

## AutoBackupSettings
### Properties
* **backupScheduleType**: 'Automated' | 'Manual': Backup schedule type.
* **backupSystemDbs**: bool: Include or exclude system databases from auto backup.
* **enable**: bool: Enable or disable autobackup on SQL virtual machine.
* **enableEncryption**: bool: Enable or disable encryption for backup on SQL virtual machine.
* **fullBackupFrequency**: 'Daily' | 'Weekly': Frequency of full backups. In both cases, full backups begin during the next scheduled time window.
* **fullBackupStartTime**: int: Start time of a given day during which full backups can take place. 0-23 hours.
* **fullBackupWindowHours**: int: Duration of the time window of a given day during which full backups can take place. 1-23 hours.
* **logBackupFrequency**: int: Frequency of log backups. 5-60 minutes.
* **password**: string (WriteOnly): Password for encryption on backup.
* **retentionPeriod**: int: Retention period of backup: 1-30 days.
* **storageAccessKey**: string (WriteOnly): Storage account key where backup will be taken to.
* **storageAccountUrl**: string: Storage account url where backup will be taken to.

## AutoPatchingSettings
### Properties
* **dayOfWeek**: 'Friday' | 'Monday' | 'Saturday' | 'Sunday' | 'Thursday' | 'Tuesday' | 'Wednesday': Day of week to apply the patch on.
* **enable**: bool: Enable or disable autopatching on SQL virtual machine.
* **maintenanceWindowDuration**: int: Duration of patching.
* **maintenanceWindowStartingHour**: int: Hour of the day when patching is initiated. Local VM time.

## KeyVaultCredentialSettings
### Properties
* **azureKeyVaultUrl**: string: Azure Key Vault url.
* **credentialName**: string: Credential name.
* **enable**: bool: Enable or disable key vault credential setting.
* **servicePrincipalName**: string: Service principal name to access key vault.
* **servicePrincipalSecret**: string (WriteOnly): Service principal name secret to access key vault.

## ServerConfigurationsManagementSettings
### Properties
* **additionalFeaturesServerConfigurations**: [AdditionalFeaturesServerConfigurations](#additionalfeaturesserverconfigurations): Additional SQL Server feature settings.
* **sqlConnectivityUpdateSettings**: [SqlConnectivityUpdateSettings](#sqlconnectivityupdatesettings): Set the access level and network port settings for SQL Server.
* **sqlStorageUpdateSettings**: [SqlStorageUpdateSettings](#sqlstorageupdatesettings): Set disk storage settings for SQL Server.
* **sqlWorkloadTypeUpdateSettings**: [SqlWorkloadTypeUpdateSettings](#sqlworkloadtypeupdatesettings): Set workload type to optimize storage for SQL Server.

## AdditionalFeaturesServerConfigurations
### Properties
* **isRServicesEnabled**: bool: Enable or disable R services (SQL 2016 onwards).

## SqlConnectivityUpdateSettings
### Properties
* **connectivityType**: 'LOCAL' | 'PRIVATE' | 'PUBLIC': SQL Server connectivity option.
* **port**: int: SQL Server port.
* **sqlAuthUpdatePassword**: string (WriteOnly): SQL Server sysadmin login password.
* **sqlAuthUpdateUserName**: string (WriteOnly): SQL Server sysadmin login to create.

## SqlStorageUpdateSettings
### Properties
* **diskConfigurationType**: 'ADD' | 'EXTEND' | 'NEW': Disk configuration to apply to SQL Server.
* **diskCount**: int: Virtual machine disk count.
* **startingDeviceId**: int: Device id of the first disk to be updated.

## SqlWorkloadTypeUpdateSettings
### Properties
* **sqlWorkloadType**: 'DW' | 'GENERAL' | 'OLTP': SQL Server workload type.

## StorageConfigurationSettings
### Properties
* **diskConfigurationType**: 'ADD' | 'EXTEND' | 'NEW': Disk configuration to apply to SQL Server.
* **sqlDataSettings**: [SQLStorageSettings](#sqlstoragesettings): Set disk storage settings for SQL Server.
* **sqlLogSettings**: [SQLStorageSettings](#sqlstoragesettings): Set disk storage settings for SQL Server.
* **sqlTempDbSettings**: [SQLStorageSettings](#sqlstoragesettings): Set disk storage settings for SQL Server.
* **storageWorkloadType**: 'DW' | 'GENERAL' | 'OLTP': Storage workload type.

## SQLStorageSettings
### Properties
* **defaultFilePath**: string: SQL Server default file path
* **luns**: int[]: Logical Unit Numbers for the disks.

## WsfcDomainCredentials
### Properties
* **clusterBootstrapAccountPassword**: string: Cluster bootstrap account password.
* **clusterOperatorAccountPassword**: string: Cluster operator account password.
* **sqlServiceAccountPassword**: string: SQL service account password.

## TrackedResourceTags
### Properties
### Additional Properties
* **Additional Properties Type**: string

