# Microsoft.HybridCompute @ 2019-12-12

## Resource Microsoft.HybridCompute/machines@2019-12-12
* **Valid Scope(s)**: ResourceGroup
### Properties
* **apiVersion**: '2019-12-12' (ReadOnly, DeployTimeConstant): The resource api version
* **id**: string (ReadOnly, DeployTimeConstant): The resource id
* **identity**: [MachineIdentity](#machineidentity)
* **location**: string (Required): The geo-location where the resource lives
* **name**: string (Required, DeployTimeConstant): The resource name
* **properties**: [MachineProperties](#machineproperties): Hybrid Compute Machine properties
* **tags**: [TrackedResourceTags](#trackedresourcetags): Resource tags.
* **type**: 'Microsoft.HybridCompute/machines' (ReadOnly, DeployTimeConstant): The resource type

## Resource Microsoft.HybridCompute/machines/extensions@2019-12-12
* **Valid Scope(s)**: ResourceGroup
### Properties
* **apiVersion**: '2019-12-12' (ReadOnly, DeployTimeConstant): The resource api version
* **id**: string (ReadOnly, DeployTimeConstant): The resource id
* **location**: string (Required): The geo-location where the resource lives
* **name**: string (Required, DeployTimeConstant): The resource name
* **properties**: [MachineExtensionProperties](#machineextensionproperties): Describes Machine Extension Properties.
* **tags**: [TrackedResourceTags](#trackedresourcetags): Resource tags.
* **type**: 'Microsoft.HybridCompute/machines/extensions' (ReadOnly, DeployTimeConstant): The resource type

## MachineIdentity
### Properties
* **principalId**: string (ReadOnly): The principal ID of resource identity.
* **tenantId**: string (ReadOnly): The tenant ID of resource.
* **type**: 'SystemAssigned': The identity type.

## MachineProperties
### Properties
* **agentVersion**: string (ReadOnly): The hybrid machine agent full version.
* **clientPublicKey**: string: Public Key that the client provides to be used during initial resource onboarding
* **displayName**: string (ReadOnly): Specifies the hybrid machine display name.
* **errorDetails**: [ErrorDetail](#errordetail)[] (ReadOnly): Details about the error state.
* **extensions**: [MachineExtensionInstanceView](#machineextensioninstanceview)[]: Machine Extensions information
* **lastStatusChange**: string (ReadOnly): The time of the last status change.
* **locationData**: [LocationData](#locationdata): Metadata pertaining to the geographic location of the resource.
* **machineFqdn**: string (ReadOnly): Specifies the hybrid machine FQDN.
* **osName**: string (ReadOnly): The Operating System running on the hybrid machine.
* **osProfile**: [MachinePropertiesOsProfile](#machinepropertiesosprofile): Specifies the operating system settings for the hybrid machine.
* **osVersion**: string (ReadOnly): The version of Operating System running on the hybrid machine.
* **provisioningState**: string (ReadOnly): The provisioning state, which only appears in the response.
* **status**: 'Connected' | 'Disconnected' | 'Error' (ReadOnly): The status of the hybrid machine agent.
* **vmId**: string: Specifies the hybrid machine unique ID.

## ErrorDetail
### Properties
* **code**: string (Required): The error's code.
* **details**: [ErrorDetail](#errordetail)[]: Additional error details.
* **message**: string (Required): A human readable error message.
* **target**: string: Indicates which property in the request is responsible for the error.

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

## MachinePropertiesOsProfile
### Properties
* **computerName**: string (ReadOnly): Specifies the host OS name of the hybrid machine.

## TrackedResourceTags
### Properties
### Additional Properties
* **Additional Properties Type**: string

## MachineExtensionProperties
### Properties
* **autoUpgradeMinorVersion**: bool: Indicates whether the extension should use a newer minor version if one is available at deployment time. Once deployed, however, the extension will not upgrade minor versions unless redeployed, even with this property set to true.
* **forceUpdateTag**: string: How the extension handler should be forced to update even if the extension configuration has not changed.
* **instanceView**: [MachineExtensionPropertiesInstanceView](#machineextensionpropertiesinstanceview): The machine extension instance view.
* **protectedSettings**: any: Any object
* **provisioningState**: string (ReadOnly): The provisioning state, which only appears in the response.
* **publisher**: string: The name of the extension handler publisher.
* **settings**: any: Any object
* **type**: string: Specifies the type of the extension; an example is "CustomScriptExtension".
* **typeHandlerVersion**: string: Specifies the version of the script handler.

## MachineExtensionPropertiesInstanceView
### Properties
* **name**: string: The machine extension name.
* **status**: [MachineExtensionInstanceViewStatus](#machineextensioninstanceviewstatus): Instance view status.
* **type**: string: Specifies the type of the extension; an example is "CustomScriptExtension".
* **typeHandlerVersion**: string: Specifies the version of the script handler.

## TrackedResourceTags
### Properties
### Additional Properties
* **Additional Properties Type**: string

