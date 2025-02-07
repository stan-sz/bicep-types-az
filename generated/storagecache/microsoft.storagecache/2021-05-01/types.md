# Microsoft.StorageCache @ 2021-05-01

## Resource Microsoft.StorageCache/caches@2021-05-01
* **Valid Scope(s)**: ResourceGroup
### Properties
* **apiVersion**: '2021-05-01' (ReadOnly, DeployTimeConstant): The resource api version
* **id**: string (ReadOnly, DeployTimeConstant): The resource id
* **identity**: [CacheIdentity](#cacheidentity): Cache identity properties.
* **location**: string: Region name string.
* **name**: string (Required, DeployTimeConstant): The resource name
* **properties**: [CacheProperties](#cacheproperties): Properties of the Cache.
* **sku**: [CacheSku](#cachesku): SKU for the Cache.
* **systemData**: [SystemData](#systemdata) (ReadOnly): Metadata pertaining to creation and last modification of the resource.
* **tags**: [CacheTags](#cachetags): Resource tags.
* **type**: 'Microsoft.StorageCache/caches' (ReadOnly, DeployTimeConstant): The resource type

## Resource Microsoft.StorageCache/caches/storageTargets@2021-05-01
* **Valid Scope(s)**: ResourceGroup
### Properties
* **apiVersion**: '2021-05-01' (ReadOnly, DeployTimeConstant): The resource api version
* **id**: string (ReadOnly, DeployTimeConstant): The resource id
* **location**: string (ReadOnly): Region name string.
* **name**: string (Required, DeployTimeConstant): The resource name
* **properties**: [StorageTargetProperties](#storagetargetproperties): Properties of the Storage Target.
* **systemData**: [SystemData](#systemdata) (ReadOnly): Metadata pertaining to creation and last modification of the resource.
* **type**: 'Microsoft.StorageCache/caches/storageTargets' (ReadOnly, DeployTimeConstant): The resource type

## CacheIdentity
### Properties
* **principalId**: string (ReadOnly): The principal ID for the system-assigned identity of the cache.
* **tenantId**: string (ReadOnly): The tenant ID associated with the cache.
* **type**: 'None' | 'SystemAssigned' | 'SystemAssigned, UserAssigned' | 'UserAssigned': The type of identity used for the cache
* **userAssignedIdentities**: [CacheIdentityUserAssignedIdentities](#cacheidentityuserassignedidentities): A dictionary where each key is a user assigned identity resource ID, and each key's value is an empty dictionary.

## CacheIdentityUserAssignedIdentities
### Properties
### Additional Properties
* **Additional Properties Type**: [UserAssignedIdentitiesValue](#userassignedidentitiesvalue)

## UserAssignedIdentitiesValue
### Properties
* **clientId**: string (ReadOnly): The client ID of the user-assigned identity.
* **principalId**: string (ReadOnly): The principal ID of the user-assigned identity.

## CacheProperties
### Properties
* **cacheSizeGB**: int: The size of this Cache, in GB.
* **directoryServicesSettings**: [CacheDirectorySettings](#cachedirectorysettings): Cache Directory Services settings.
* **encryptionSettings**: [CacheEncryptionSettings](#cacheencryptionsettings): Cache encryption settings.
* **health**: [CacheHealth](#cachehealth) (ReadOnly): An indication of Cache health. Gives more information about health than just that related to provisioning.
* **mountAddresses**: string[] (ReadOnly): Array of IP addresses that can be used by clients mounting this Cache.
* **networkSettings**: [CacheNetworkSettings](#cachenetworksettings): Cache network settings.
* **provisioningState**: 'Cancelled' | 'Creating' | 'Deleting' | 'Failed' | 'Succeeded' | 'Updating' (ReadOnly): ARM provisioning state, see https://github.com/Azure/azure-resource-manager-rpc/blob/master/v1.0/Addendum.md#provisioningstate-property
* **securitySettings**: [CacheSecuritySettings](#cachesecuritysettings): Cache security settings.
* **subnet**: string: A fully qualified URL.
* **upgradeStatus**: [CacheUpgradeStatus](#cacheupgradestatus) (ReadOnly): Properties describing the software upgrade state of the Cache.

## CacheDirectorySettings
### Properties
* **activeDirectory**: [CacheActiveDirectorySettings](#cacheactivedirectorysettings): Active Directory settings used to join a cache to a domain.
* **usernameDownload**: [CacheUsernameDownloadSettings](#cacheusernamedownloadsettings): Settings for Extended Groups username and group download.

## CacheActiveDirectorySettings
### Properties
* **cacheNetBiosName**: string (Required): The NetBIOS name to assign to the HPC Cache when it joins the Active Directory domain as a server. Length must 1-15 characters from the class [-0-9a-zA-Z].
* **credentials**: [CacheActiveDirectorySettingsCredentials](#cacheactivedirectorysettingscredentials): Active Directory admin credentials used to join the HPC Cache to a domain.
* **domainJoined**: 'Error' | 'No' | 'Yes' (ReadOnly): True if the HPC Cache is joined to the Active Directory domain.
* **domainName**: string (Required): The fully qualified domain name of the Active Directory domain controller.
* **domainNetBiosName**: string (Required): The Active Directory domain's NetBIOS name.
* **primaryDnsIpAddress**: string (Required): Primary DNS IP address used to resolve the Active Directory domain controller's fully qualified domain name.
* **secondaryDnsIpAddress**: string: Secondary DNS IP address used to resolve the Active Directory domain controller's fully qualified domain name.

## CacheActiveDirectorySettingsCredentials
### Properties
* **password**: string (Required): Plain text password of the Active Directory domain administrator. This value is stored encrypted and not returned on response.
* **username**: string (Required): Username of the Active Directory domain administrator. This value is stored encrypted and not returned on response.

## CacheUsernameDownloadSettings
### Properties
* **autoDownloadCertificate**: bool: Determines if the certificate should be automatically downloaded. This applies to 'caCertificateURI' only if 'requireValidCertificate' is true.
* **caCertificateURI**: string: The URI of the CA certificate to validate the LDAP secure connection. This field must be populated when 'requireValidCertificate' is set to true.
* **credentials**: [CacheUsernameDownloadSettingsCredentials](#cacheusernamedownloadsettingscredentials): When present, these are the credentials for the secure LDAP connection.
* **encryptLdapConnection**: bool: Whether or not the LDAP connection should be encrypted.
* **extendedGroups**: bool: Whether or not Extended Groups is enabled.
* **groupFileURI**: string: The URI of the file containing group information (in /etc/group file format). This field must be populated when 'usernameSource' is set to 'File'.
* **ldapBaseDN**: string: The base distinguished name for the LDAP domain.
* **ldapServer**: string: The fully qualified domain name or IP address of the LDAP server to use.
* **requireValidCertificate**: bool: Determines if the certificates must be validated by a certificate authority. When true, caCertificateURI must be provided.
* **userFileURI**: string: The URI of the file containing user information (in /etc/passwd file format). This field must be populated when 'usernameSource' is set to 'File'.
* **usernameDownloaded**: 'Error' | 'No' | 'Yes' (ReadOnly): Indicates whether or not the HPC Cache has performed the username download successfully.
* **usernameSource**: 'AD' | 'File' | 'LDAP' | 'None': This setting determines how the cache gets username and group names for clients.

## CacheUsernameDownloadSettingsCredentials
### Properties
* **bindDn**: string: The Bind Distinguished Name identity to be used in the secure LDAP connection. This value is stored encrypted and not returned on response.
* **bindPassword**: string: The Bind password to be used in the secure LDAP connection. This value is stored encrypted and not returned on response.

## CacheEncryptionSettings
### Properties
* **keyEncryptionKey**: [KeyVaultKeyReference](#keyvaultkeyreference): Describes a reference to Key Vault Key.
* **rotationToLatestKeyVersionEnabled**: bool: Specifies whether the service will automatically rotate to the newest version of the key in the Key Vault.

## KeyVaultKeyReference
### Properties
* **keyUrl**: string (Required): The URL referencing a key encryption key in Key Vault.
* **sourceVault**: [KeyVaultKeyReferenceSourceVault](#keyvaultkeyreferencesourcevault) (Required): Describes a resource Id to source Key Vault.

## KeyVaultKeyReferenceSourceVault
### Properties
* **id**: string: Resource Id.

## CacheHealth
### Properties
* **conditions**: [Condition](#condition)[] (ReadOnly): Outstanding conditions that need to be investigated and resolved.
* **state**: 'Degraded' | 'Down' | 'Flushing' | 'Healthy' | 'Stopped' | 'Stopping' | 'Transitioning' | 'Unknown' | 'Upgrading': List of Cache health states.
* **statusDescription**: string: Describes explanation of state.

## Condition
### Properties
* **message**: string (ReadOnly): The issue requiring attention.
* **timestamp**: string (ReadOnly): The time when the condition was raised.

## CacheNetworkSettings
### Properties
* **dnsSearchDomain**: string: DNS search domain
* **dnsServers**: string[]: DNS servers for the cache to use.  It will be set from the network configuration if no value is provided.
* **mtu**: int: The IPv4 maximum transmission unit configured for the subnet.
* **ntpServer**: string: NTP server IP Address or FQDN for the cache to use. The default is time.windows.com.
* **utilityAddresses**: string[] (ReadOnly): Array of additional IP addresses used by this Cache.

## CacheSecuritySettings
### Properties
* **accessPolicies**: [NfsAccessPolicy](#nfsaccesspolicy)[]: NFS access policies defined for this cache.

## NfsAccessPolicy
### Properties
* **accessRules**: [NfsAccessRule](#nfsaccessrule)[] (Required): The set of rules describing client accesses allowed under this policy.
* **name**: string (Required): Name identifying this policy. Access Policy names are not case sensitive.

## NfsAccessRule
### Properties
* **access**: 'no' | 'ro' | 'rw' (Required): Access allowed by this rule.
* **anonymousGID**: string: GID value that replaces 0 when rootSquash is true. This will use the value of anonymousUID if not provided.
* **anonymousUID**: string: UID value that replaces 0 when rootSquash is true. 65534 will be used if not provided.
* **filter**: string: Filter applied to the scope for this rule. The filter's format depends on its scope. 'default' scope matches all clients and has no filter value. 'network' scope takes a filter in CIDR format (for example, 10.99.1.0/24). 'host' takes an IP address or fully qualified domain name as filter. If a client does not match any filter rule and there is no default rule, access is denied.
* **rootSquash**: bool: Map root accesses to anonymousUID and anonymousGID.
* **scope**: 'default' | 'host' | 'network' (Required): Scope for this rule. The scope and filter determine which clients match the rule.
* **submountAccess**: bool: For the default policy, allow access to subdirectories under the root export. If this is set to no, clients can only mount the path '/'. If set to yes, clients can mount a deeper path, like '/a/b'.
* **suid**: bool: Allow SUID semantics.

## CacheUpgradeStatus
### Properties
* **currentFirmwareVersion**: string (ReadOnly): Version string of the firmware currently installed on this Cache.
* **firmwareUpdateDeadline**: string (ReadOnly): Time at which the pending firmware update will automatically be installed on the Cache.
* **firmwareUpdateStatus**: 'available' | 'unavailable' (ReadOnly): True if there is a firmware update ready to install on this Cache. The firmware will automatically be installed after firmwareUpdateDeadline if not triggered earlier via the upgrade operation.
* **lastFirmwareUpdate**: string (ReadOnly): Time of the last successful firmware update.
* **pendingFirmwareVersion**: string (ReadOnly): When firmwareUpdateAvailable is true, this field holds the version string for the update.

## CacheSku
### Properties
* **name**: string: SKU name for this Cache.

## SystemData
### Properties
* **createdAt**: string: The timestamp of resource creation (UTC).
* **createdBy**: string: The identity that created the resource.
* **createdByType**: 'Application' | 'Key' | 'ManagedIdentity' | 'User': The type of identity that created the resource.
* **lastModifiedAt**: string: The timestamp of resource last modification (UTC)
* **lastModifiedBy**: string: The identity that last modified the resource.
* **lastModifiedByType**: 'Application' | 'Key' | 'ManagedIdentity' | 'User': The type of identity that created the resource.

## CacheTags
### Properties
### Additional Properties
* **Additional Properties Type**: string

## StorageTargetProperties
### Properties
* **blobNfs**: [BlobNfsTarget](#blobnfstarget): Properties pertaining to the BlobNfsTarget.
* **clfs**: [ClfsTarget](#clfstarget): Properties pertaining to the ClfsTarget
* **junctions**: [NamespaceJunction](#namespacejunction)[]: List of Cache namespace junctions to target for namespace associations.
* **nfs3**: [Nfs3Target](#nfs3target): Properties pertaining to the Nfs3Target
* **provisioningState**: 'Cancelled' | 'Creating' | 'Deleting' | 'Failed' | 'Succeeded' | 'Updating' (ReadOnly): ARM provisioning state, see https://github.com/Azure/azure-resource-manager-rpc/blob/master/v1.0/Addendum.md#provisioningstate-property
* **targetType**: 'blobNfs' | 'clfs' | 'nfs3' | 'unknown' (Required): Type of the Storage Target.
* **unknown**: [UnknownTarget](#unknowntarget): Properties pertaining to the UnknownTarget

## BlobNfsTarget
### Properties
* **target**: string: A fully qualified URL.
* **usageModel**: string: Identifies the StorageCache usage model to be used for this storage target.

## ClfsTarget
### Properties
* **target**: string: A fully qualified URL.

## NamespaceJunction
### Properties
* **namespacePath**: string: Namespace path on a Cache for a Storage Target.
* **nfsAccessPolicy**: string: Name of the access policy applied to this junction.
* **nfsExport**: string: NFS export where targetPath exists.
* **targetPath**: string: Path in Storage Target to which namespacePath points.

## Nfs3Target
### Properties
* **target**: string: IP address or host name of an NFSv3 host (e.g., 10.0.44.44).
* **usageModel**: string: Identifies the StorageCache usage model to be used for this storage target.

## UnknownTarget
### Properties
* **attributes**: [UnknownProperties](#unknownproperties): Properties of an unknown type of Storage Target.

## UnknownProperties
### Properties
### Additional Properties
* **Additional Properties Type**: string

