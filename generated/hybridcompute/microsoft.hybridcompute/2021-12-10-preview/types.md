# Microsoft.HybridCompute @ 2021-12-10-preview

## Resource Microsoft.HybridCompute/machines@2021-12-10-preview
* **Valid Scope(s)**: ResourceGroup
### Properties
* **apiVersion**: '2021-12-10-preview' (ReadOnly, DeployTimeConstant): The resource api version
* **id**: string (ReadOnly, DeployTimeConstant): The resource id
* **identity**: [Identity](#identity): Identity for the resource.
* **location**: string (Required): The geo-location where the resource lives
* **name**: string (Required, DeployTimeConstant): The resource name
* **properties**: [MachineProperties](#machineproperties): Describes the properties of a hybrid machine.
* **systemData**: [SystemData](#systemdata) (ReadOnly): Metadata pertaining to creation and last modification of the resource.
* **tags**: [TrackedResourceTags](#trackedresourcetags): Resource tags.
* **type**: 'Microsoft.HybridCompute/machines' (ReadOnly, DeployTimeConstant): The resource type

## Resource Microsoft.HybridCompute/machines/extensions@2021-12-10-preview
* **Valid Scope(s)**: ResourceGroup
### Properties
* **apiVersion**: '2021-12-10-preview' (ReadOnly, DeployTimeConstant): The resource api version
* **id**: string (ReadOnly, DeployTimeConstant): The resource id
* **location**: string (Required): The geo-location where the resource lives
* **name**: string (Required, DeployTimeConstant): The resource name
* **properties**: [MachineExtensionProperties](#machineextensionproperties): Describes the properties of a Machine Extension.
* **systemData**: [SystemData](#systemdata) (ReadOnly): Metadata pertaining to creation and last modification of the resource.
* **tags**: [TrackedResourceTags](#trackedresourcetags): Resource tags.
* **type**: 'Microsoft.HybridCompute/machines/extensions' (ReadOnly, DeployTimeConstant): The resource type

## Resource Microsoft.HybridCompute/privateLinkScopes@2021-12-10-preview
* **Valid Scope(s)**: ResourceGroup
### Properties
* **apiVersion**: '2021-12-10-preview' (ReadOnly, DeployTimeConstant): The resource api version
* **id**: string (ReadOnly, DeployTimeConstant): The resource id
* **location**: string (Required): Resource location
* **name**: string (Required, DeployTimeConstant): The resource name
* **properties**: [HybridComputePrivateLinkScopeProperties](#hybridcomputeprivatelinkscopeproperties): Properties that define a Azure Arc PrivateLinkScope resource.
* **systemData**: [SystemData](#systemdata) (ReadOnly): Metadata pertaining to creation and last modification of the resource.
* **tags**: [PrivateLinkScopesResourceTags](#privatelinkscopesresourcetags): Resource tags
* **type**: 'Microsoft.HybridCompute/privateLinkScopes' (ReadOnly, DeployTimeConstant): The resource type

## Resource Microsoft.HybridCompute/privateLinkScopes/privateEndpointConnections@2021-12-10-preview
* **Valid Scope(s)**: ResourceGroup
### Properties
* **apiVersion**: '2021-12-10-preview' (ReadOnly, DeployTimeConstant): The resource api version
* **id**: string (ReadOnly, DeployTimeConstant): The resource id
* **name**: string (Required, DeployTimeConstant): The resource name
* **properties**: [PrivateEndpointConnectionProperties](#privateendpointconnectionproperties): Properties of a private endpoint connection.
* **systemData**: [SystemData](#systemdata) (ReadOnly): Metadata pertaining to creation and last modification of the resource.
* **type**: 'Microsoft.HybridCompute/privateLinkScopes/privateEndpointConnections' (ReadOnly, DeployTimeConstant): The resource type

## Identity
### Properties
* **principalId**: string (ReadOnly): The principal ID of resource identity.
* **tenantId**: string (ReadOnly): The tenant ID of resource.
* **type**: 'SystemAssigned': The identity type.

## MachineProperties
### Properties
* **adFqdn**: string (ReadOnly): Specifies the AD fully qualified display name.
* **agentConfiguration**: [AgentConfiguration](#agentconfiguration): Configurable properties that the user can set locally via the azcmagent config command, or remotely via ARM.
* **agentVersion**: string (ReadOnly): The hybrid machine agent full version.
* **clientPublicKey**: string: Public Key that the client provides to be used during initial resource onboarding
* **cloudMetadata**: [CloudMetadata](#cloudmetadata): The metadata of the cloud environment (Azure/GCP/AWS/OCI...).
* **detectedProperties**: [DetectedProperties](#detectedproperties) (ReadOnly): Detected properties from the machine.
* **displayName**: string (ReadOnly): Specifies the hybrid machine display name.
* **dnsFqdn**: string (ReadOnly): Specifies the DNS fully qualified display name.
* **domainName**: string (ReadOnly): Specifies the Windows domain name.
* **errorDetails**: [ErrorDetail](#errordetail)[] (ReadOnly): Details about the error state.
* **extensions**: [MachineExtensionInstanceView](#machineextensioninstanceview)[]: Machine Extensions information
* **lastStatusChange**: string (ReadOnly): The time of the last status change.
* **locationData**: [LocationData](#locationdata): Metadata pertaining to the geographic location of the resource.
* **machineFqdn**: string (ReadOnly): Specifies the hybrid machine FQDN.
* **mssqlDiscovered**: string: Specifies whether any MS SQL instance is discovered on the machine.
* **osName**: string (ReadOnly): The Operating System running on the hybrid machine.
* **osProfile**: [OSProfile](#osprofile): Specifies the operating system settings for the hybrid machine.
* **osSku**: string (ReadOnly): Specifies the Operating System product SKU.
* **osType**: string: The type of Operating System (windows/linux).
* **osVersion**: string (ReadOnly): The version of Operating System running on the hybrid machine.
* **parentClusterResourceId**: string: The resource id of the parent cluster (Azure HCI) this machine is assigned to, if any.
* **privateLinkScopeResourceId**: string: The resource id of the private link scope this machine is assigned to, if any.
* **provisioningState**: string (ReadOnly): The provisioning state, which only appears in the response.
* **status**: 'Connected' | 'Disconnected' | 'Error' (ReadOnly): The status of the hybrid machine agent.
* **vmId**: string: Specifies the hybrid machine unique ID.
* **vmUuid**: string (ReadOnly): Specifies the Arc Machine's unique SMBIOS ID

## AgentConfiguration
### Properties
* **incomingConnectionsPorts**: string[] (ReadOnly): Specifies the list of ports that the agent will be able to listen on.
* **proxyUrl**: string (ReadOnly): Specifies the URL of the proxy to be used.

## CloudMetadata
### Properties
* **provider**: string (ReadOnly): Specifies the cloud provider (Azure/AWS/GCP...).

## DetectedProperties
### Properties
### Additional Properties
* **Additional Properties Type**: string

## ErrorDetail
### Properties
* **additionalInfo**: [ErrorAdditionalInfo](#erroradditionalinfo)[] (ReadOnly): The error additional info.
* **code**: string (ReadOnly): The error code.
* **details**: [ErrorDetail](#errordetail)[] (ReadOnly): The error details.
* **message**: string (ReadOnly): The error message.
* **target**: string (ReadOnly): The error target.

## ErrorAdditionalInfo
### Properties
* **info**: any (ReadOnly): Any object
* **type**: string (ReadOnly): The additional info type.

## MachineExtensionInstanceView
### Properties
* **name**: string: The machine extension name.
* **status**: [MachineExtensionInstanceViewStatus](#machineextensioninstanceviewstatus): Instance view status.
* **type**: string: Specifies the type of the extension; an example is "CustomScriptExtension".
* **typeHandlerVersion**: string: Specifies the version of the script handler.

## MachineExtensionInstanceViewStatus
### Properties
* **code**: string: The status code.
* **displayStatus**: string: The short localizable label for the status.
* **level**: 'Error' | 'Info' | 'Warning': The level code.
* **message**: string: The detailed status message, including for alerts and error messages.
* **time**: string: The time of the status.

## LocationData
### Properties
* **city**: string: The city or locality where the resource is located.
* **countryOrRegion**: string: The country or region where the resource is located
* **district**: string: The district, state, or province where the resource is located.
* **name**: string (Required): A canonical name for the geographic or physical location.

## OSProfile
### Properties
* **computerName**: string (ReadOnly): Specifies the host OS name of the hybrid machine.
* **linuxConfiguration**: [OSProfileLinuxConfiguration](#osprofilelinuxconfiguration): Specifies the linux configuration for update management.
* **windowsConfiguration**: [OSProfileWindowsConfiguration](#osprofilewindowsconfiguration): Specifies the windows configuration for update management.

## OSProfileLinuxConfiguration
### Properties
* **patchSettings**: [PatchSettings](#patchsettings): Specifies the patch settings.

## PatchSettings
### Properties
* **assessmentMode**: string: Specifies the assessment mode.
* **patchMode**: string: Specifies the patch mode.

## OSProfileWindowsConfiguration
### Properties
* **patchSettings**: [PatchSettings](#patchsettings): Specifies the patch settings.

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

## MachineExtensionProperties
### Properties
* **autoUpgradeMinorVersion**: bool: Indicates whether the extension should use a newer minor version if one is available at deployment time. Once deployed, however, the extension will not upgrade minor versions unless redeployed, even with this property set to true.
* **enableAutomaticUpgrade**: bool: Indicates whether the extension should be automatically upgraded by the platform if there is a newer version available.
* **forceUpdateTag**: string: How the extension handler should be forced to update even if the extension configuration has not changed.
* **instanceView**: [MachineExtensionInstanceView](#machineextensioninstanceview): Describes the Machine Extension Instance View.
* **protectedSettings**: any: Any object
* **provisioningState**: string (ReadOnly): The provisioning state, which only appears in the response.
* **publisher**: string: The name of the extension handler publisher.
* **settings**: any: Any object
* **type**: string: Specifies the type of the extension; an example is "CustomScriptExtension".
* **typeHandlerVersion**: string: Specifies the version of the script handler.

## TrackedResourceTags
### Properties
### Additional Properties
* **Additional Properties Type**: string

## HybridComputePrivateLinkScopeProperties
### Properties
* **privateEndpointConnections**: [PrivateEndpointConnectionDataModel](#privateendpointconnectiondatamodel)[] (ReadOnly): The collection of associated Private Endpoint Connections.
* **privateLinkScopeId**: string (ReadOnly): The Guid id of the private link scope.
* **provisioningState**: string (ReadOnly): Current state of this PrivateLinkScope: whether or not is has been provisioned within the resource group it is defined. Users cannot change this value but are able to read from it. Values will include Provisioning ,Succeeded, Canceled and Failed.
* **publicNetworkAccess**: 'Disabled' | 'Enabled': The network access policy to determine if Azure Arc agents can use public Azure Arc service endpoints. Defaults to disabled (access to Azure Arc services only via private link).

## PrivateEndpointConnectionDataModel
### Properties
* **id**: string (ReadOnly): The ARM Resource Id of the Private Endpoint.
* **name**: string (ReadOnly): The Name of the Private Endpoint.
* **properties**: [PrivateEndpointConnectionProperties](#privateendpointconnectionproperties): Properties of a private endpoint connection.
* **type**: string (ReadOnly): Azure resource type

## PrivateEndpointConnectionProperties
### Properties
* **privateEndpoint**: [PrivateEndpointProperty](#privateendpointproperty): Private endpoint which the connection belongs to.
* **privateLinkServiceConnectionState**: [PrivateLinkServiceConnectionStateProperty](#privatelinkserviceconnectionstateproperty): State of the private endpoint connection.
* **provisioningState**: string (ReadOnly): State of the private endpoint connection.

## PrivateEndpointProperty
### Properties
* **id**: string: Resource id of the private endpoint.

## PrivateLinkServiceConnectionStateProperty
### Properties
* **actionsRequired**: string (ReadOnly): The actions required for private link service connection.
* **description**: string (Required): The private link service connection description.
* **status**: string (Required): The private link service connection status.

## PrivateLinkScopesResourceTags
### Properties
### Additional Properties
* **Additional Properties Type**: string

