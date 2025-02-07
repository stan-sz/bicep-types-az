# Microsoft.ContainerInstance @ 2021-07-01

## Resource Microsoft.ContainerInstance/containerGroups@2021-07-01
* **Valid Scope(s)**: ResourceGroup
### Properties
* **apiVersion**: '2021-07-01' (ReadOnly, DeployTimeConstant): The resource api version
* **id**: string (ReadOnly, DeployTimeConstant): The resource id
* **identity**: [ContainerGroupIdentity](#containergroupidentity): Identity for the container group.
* **location**: string: The resource location.
* **name**: string (Required, DeployTimeConstant): The resource name
* **properties**: [ContainerGroupProperties](#containergroupproperties) (Required): The container group properties
* **tags**: [ResourceTags](#resourcetags): The resource tags.
* **type**: 'Microsoft.ContainerInstance/containerGroups' (ReadOnly, DeployTimeConstant): The resource type

## ContainerGroupIdentity
### Properties
* **principalId**: string (ReadOnly): The principal id of the container group identity. This property will only be provided for a system assigned identity.
* **tenantId**: string (ReadOnly): The tenant id associated with the container group. This property will only be provided for a system assigned identity.
* **type**: 'None' | 'SystemAssigned' | 'SystemAssigned, UserAssigned' | 'UserAssigned': The type of identity used for the container group. The type 'SystemAssigned, UserAssigned' includes both an implicitly created identity and a set of user assigned identities. The type 'None' will remove any identities from the container group.
* **userAssignedIdentities**: [ContainerGroupIdentityUserAssignedIdentities](#containergroupidentityuserassignedidentities): The list of user identities associated with the container group. The user identity dictionary key references will be ARM resource ids in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/userAssignedIdentities/{identityName}'.

## ContainerGroupIdentityUserAssignedIdentities
### Properties
### Additional Properties
* **Additional Properties Type**: [Components10Wh5UdSchemasContainergroupidentityPropertiesUserassignedidentitiesAdditionalproperties](#components10wh5udschemascontainergroupidentitypropertiesuserassignedidentitiesadditionalproperties)

## Components10Wh5UdSchemasContainergroupidentityPropertiesUserassignedidentitiesAdditionalproperties
### Properties
* **clientId**: string (ReadOnly): The client id of user assigned identity.
* **principalId**: string (ReadOnly): The principal id of user assigned identity.

## ContainerGroupProperties
### Properties
* **containers**: [Container](#container)[] (Required): The containers within the container group.
* **diagnostics**: [ContainerGroupDiagnostics](#containergroupdiagnostics): Container group diagnostic information.
* **dnsConfig**: [DnsConfiguration](#dnsconfiguration): DNS configuration for the container group.
* **encryptionProperties**: [EncryptionProperties](#encryptionproperties): The container group encryption properties.
* **imageRegistryCredentials**: [ImageRegistryCredential](#imageregistrycredential)[]: The image registry credentials by which the container group is created from.
* **initContainers**: [InitContainerDefinition](#initcontainerdefinition)[]: The init containers for a container group.
* **instanceView**: [ContainerGroupPropertiesInstanceView](#containergrouppropertiesinstanceview) (ReadOnly): The instance view of the container group. Only valid in response.
* **ipAddress**: [IpAddress](#ipaddress): IP address for the container group.
* **osType**: 'Linux' | 'Windows' (Required): The operating system type required by the containers in the container group.
* **provisioningState**: string (ReadOnly): The provisioning state of the container group. This only appears in the response.
* **restartPolicy**: 'Always' | 'Never' | 'OnFailure': Restart policy for all containers within the container group. 
- `Always` Always restart
- `OnFailure` Restart on failure
- `Never` Never restart
* **sku**: 'Dedicated' | 'Standard': The container group SKU.
* **subnetIds**: [ContainerGroupSubnetId](#containergroupsubnetid)[]: The subnet resource IDs for a container group.
* **volumes**: [Volume](#volume)[]: The list of volumes that can be mounted by containers in this container group.

## Container
### Properties
* **name**: string (Required): The user-provided name of the container instance.
* **properties**: [ContainerProperties](#containerproperties) (Required): The container instance properties.

## ContainerProperties
### Properties
* **command**: string[]: The commands to execute within the container instance in exec form.
* **environmentVariables**: [EnvironmentVariable](#environmentvariable)[]: The environment variables to set in the container instance.
* **image**: string (Required): The name of the image used to create the container instance.
* **instanceView**: [ContainerPropertiesInstanceView](#containerpropertiesinstanceview) (ReadOnly): The instance view of the container instance. Only valid in response.
* **livenessProbe**: [ContainerProbe](#containerprobe): The container probe, for liveness or readiness
* **ports**: [ContainerPort](#containerport)[]: The exposed ports on the container instance.
* **readinessProbe**: [ContainerProbe](#containerprobe): The container probe, for liveness or readiness
* **resources**: [ResourceRequirements](#resourcerequirements) (Required): The resource requirements.
* **volumeMounts**: [VolumeMount](#volumemount)[]: The volume mounts available to the container instance.

## EnvironmentVariable
### Properties
* **name**: string (Required): The name of the environment variable.
* **secureValue**: string: The value of the secure environment variable.
* **value**: string: The value of the environment variable.

## ContainerPropertiesInstanceView
### Properties
* **currentState**: [ContainerState](#containerstate) (ReadOnly): The container instance state.
* **events**: [Event](#event)[] (ReadOnly): The events of the container instance.
* **previousState**: [ContainerState](#containerstate) (ReadOnly): The container instance state.
* **restartCount**: int (ReadOnly): The number of times that the container instance has been restarted.

## ContainerState
### Properties
* **detailStatus**: string (ReadOnly): The human-readable status of the container instance state.
* **exitCode**: int (ReadOnly): The container instance exit codes correspond to those from the `docker run` command.
* **finishTime**: string (ReadOnly): The date-time when the container instance state finished.
* **startTime**: string (ReadOnly): The date-time when the container instance state started.
* **state**: string (ReadOnly): The state of the container instance.

## Event
### Properties
* **count**: int (ReadOnly): The count of the event.
* **firstTimestamp**: string (ReadOnly): The date-time of the earliest logged event.
* **lastTimestamp**: string (ReadOnly): The date-time of the latest logged event.
* **message**: string (ReadOnly): The event message.
* **name**: string (ReadOnly): The event name.
* **type**: string (ReadOnly): The event type.

## ContainerProbe
### Properties
* **exec**: [ContainerExec](#containerexec): The container execution command, for liveness or readiness probe
* **failureThreshold**: int: The failure threshold.
* **httpGet**: [ContainerHttpGet](#containerhttpget): The container Http Get settings, for liveness or readiness probe
* **initialDelaySeconds**: int: The initial delay seconds.
* **periodSeconds**: int: The period seconds.
* **successThreshold**: int: The success threshold.
* **timeoutSeconds**: int: The timeout seconds.

## ContainerExec
### Properties
* **command**: string[]: The commands to execute within the container.

## ContainerHttpGet
### Properties
* **httpHeaders**: [HttpHeader](#httpheader)[]: The HTTP headers.
* **path**: string: The path to probe.
* **port**: int (Required): The port number to probe.
* **scheme**: 'http' | 'https': The scheme.

## HttpHeader
### Properties
* **name**: string: The header name.
* **value**: string: The header value.

## ContainerPort
### Properties
* **port**: int (Required): The port number exposed within the container group.
* **protocol**: 'TCP' | 'UDP': The protocol associated with the port.

## ResourceRequirements
### Properties
* **limits**: [ResourceLimits](#resourcelimits): The resource limits.
* **requests**: [ResourceRequests](#resourcerequests) (Required): The resource requests.

## ResourceLimits
### Properties
* **cpu**: int: The CPU limit of this container instance.
* **gpu**: [GpuResource](#gpuresource): The GPU resource.
* **memoryInGB**: int: The memory limit in GB of this container instance.

## GpuResource
### Properties
* **count**: int (Required): The count of the GPU resource.
* **sku**: 'K80' | 'P100' | 'V100' (Required): The SKU of the GPU resource.

## ResourceRequests
### Properties
* **cpu**: int (Required): The CPU request of this container instance.
* **gpu**: [GpuResource](#gpuresource): The GPU resource.
* **memoryInGB**: int (Required): The memory request in GB of this container instance.

## VolumeMount
### Properties
* **mountPath**: string (Required): The path within the container where the volume should be mounted. Must not contain colon (:).
* **name**: string (Required): The name of the volume mount.
* **readOnly**: bool: The flag indicating whether the volume mount is read-only.

## ContainerGroupDiagnostics
### Properties
* **logAnalytics**: [LogAnalytics](#loganalytics): Container group log analytics information.

## LogAnalytics
### Properties
* **logType**: 'ContainerInsights' | 'ContainerInstanceLogs': The log type to be used.
* **metadata**: [LogAnalyticsMetadata](#loganalyticsmetadata): Metadata for log analytics.
* **workspaceId**: string (Required): The workspace id for log analytics
* **workspaceKey**: string (Required): The workspace key for log analytics
* **workspaceResourceId**: string: The workspace resource id for log analytics

## LogAnalyticsMetadata
### Properties
### Additional Properties
* **Additional Properties Type**: string

## DnsConfiguration
### Properties
* **nameServers**: string[] (Required): The DNS servers for the container group.
* **options**: string: The DNS options for the container group.
* **searchDomains**: string: The DNS search domains for hostname lookup in the container group.

## EncryptionProperties
### Properties
* **keyName**: string (Required): The encryption key name.
* **keyVersion**: string (Required): The encryption key version.
* **vaultBaseUrl**: string (Required): The keyvault base url.

## ImageRegistryCredential
### Properties
* **identity**: string: The identity for the private registry.
* **identityUrl**: string: The identity URL for the private registry.
* **password**: string: The password for the private registry.
* **server**: string (Required): The Docker image registry server without a protocol such as "http" and "https".
* **username**: string (Required): The username for the private registry.

## InitContainerDefinition
### Properties
* **name**: string (Required): The name for the init container.
* **properties**: [InitContainerPropertiesDefinition](#initcontainerpropertiesdefinition) (Required): The init container definition properties.

## InitContainerPropertiesDefinition
### Properties
* **command**: string[]: The command to execute within the init container in exec form.
* **environmentVariables**: [EnvironmentVariable](#environmentvariable)[]: The environment variables to set in the init container.
* **image**: string: The image of the init container.
* **instanceView**: [InitContainerPropertiesDefinitionInstanceView](#initcontainerpropertiesdefinitioninstanceview) (ReadOnly): The instance view of the init container. Only valid in response.
* **volumeMounts**: [VolumeMount](#volumemount)[]: The volume mounts available to the init container.

## InitContainerPropertiesDefinitionInstanceView
### Properties
* **currentState**: [ContainerState](#containerstate) (ReadOnly): The container instance state.
* **events**: [Event](#event)[] (ReadOnly): The events of the init container.
* **previousState**: [ContainerState](#containerstate) (ReadOnly): The container instance state.
* **restartCount**: int (ReadOnly): The number of times that the init container has been restarted.

## ContainerGroupPropertiesInstanceView
### Properties
* **events**: [Event](#event)[] (ReadOnly): The events of this container group.
* **state**: string (ReadOnly): The state of the container group. Only valid in response.

## IpAddress
### Properties
* **dnsNameLabel**: string: The Dns name label for the IP.
* **fqdn**: string (ReadOnly): The FQDN for the IP.
* **ip**: string: The IP exposed to the public internet.
* **ports**: [Port](#port)[] (Required): The list of ports exposed on the container group.
* **type**: 'Private' | 'Public' (Required): Specifies if the IP is exposed to the public internet or private VNET.

## Port
### Properties
* **port**: int (Required): The port number.
* **protocol**: 'TCP' | 'UDP': The protocol associated with the port.

## ContainerGroupSubnetId
### Properties
* **id**: string (Required): Resource ID of virtual network and subnet.
* **name**: string: Friendly name for the subnet.

## Volume
### Properties
* **azureFile**: [AzureFileVolume](#azurefilevolume): The properties of the Azure File volume. Azure File shares are mounted as volumes.
* **emptyDir**: any: Any object
* **gitRepo**: [GitRepoVolume](#gitrepovolume): Represents a volume that is populated with the contents of a git repository
* **name**: string (Required): The name of the volume.
* **secret**: [SecretVolume](#secretvolume): The secret volume.

## AzureFileVolume
### Properties
* **readOnly**: bool: The flag indicating whether the Azure File shared mounted as a volume is read-only.
* **shareName**: string (Required): The name of the Azure File share to be mounted as a volume.
* **storageAccountKey**: string: The storage account access key used to access the Azure File share.
* **storageAccountName**: string (Required): The name of the storage account that contains the Azure File share.

## GitRepoVolume
### Properties
* **directory**: string: Target directory name. Must not contain or start with '..'.  If '.' is supplied, the volume directory will be the git repository.  Otherwise, if specified, the volume will contain the git repository in the subdirectory with the given name.
* **repository**: string (Required): Repository URL
* **revision**: string: Commit hash for the specified revision.

## SecretVolume
### Properties
### Additional Properties
* **Additional Properties Type**: string

## ResourceTags
### Properties
### Additional Properties
* **Additional Properties Type**: string

