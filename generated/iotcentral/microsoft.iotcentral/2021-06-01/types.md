# Microsoft.IoTCentral @ 2021-06-01

## Resource Microsoft.IoTCentral/iotApps@2021-06-01
* **Valid Scope(s)**: ResourceGroup
### Properties
* **apiVersion**: '2021-06-01' (ReadOnly, DeployTimeConstant): The resource api version
* **id**: string (ReadOnly, DeployTimeConstant): The resource id
* **identity**: [SystemAssignedServiceIdentity](#systemassignedserviceidentity): Managed service identity (either system assigned, or none)
* **location**: string (Required): The resource location.
* **name**: string (Required, DeployTimeConstant): The resource name
* **properties**: [AppProperties](#appproperties): The properties of an IoT Central application.
* **sku**: [AppSkuInfo](#appskuinfo) (Required): Information about the SKU of the IoT Central application.
* **tags**: [ResourceTags](#resourcetags): The resource tags.
* **type**: 'Microsoft.IoTCentral/iotApps' (ReadOnly, DeployTimeConstant): The resource type

## SystemAssignedServiceIdentity
### Properties
* **principalId**: string (ReadOnly): The service principal ID of the system assigned identity. This property will only be provided for a system assigned identity.
* **tenantId**: string (ReadOnly): The tenant ID of the system assigned identity. This property will only be provided for a system assigned identity.
* **type**: 'None' | 'SystemAssigned' (Required): Type of managed service identity (either system assigned, or none).

## AppProperties
### Properties
* **applicationId**: string (ReadOnly): The ID of the application.
* **displayName**: string: The display name of the application.
* **state**: 'created' | 'suspended' (ReadOnly): The current state of the application.
* **subdomain**: string: The subdomain of the application.
* **template**: string: The ID of the application template, which is a blueprint that defines the characteristics and behaviors of an application. Optional; if not specified, defaults to a blank blueprint and allows the application to be defined from scratch.

## AppSkuInfo
### Properties
* **name**: 'ST0' | 'ST1' | 'ST2' (Required): The name of the SKU.

## ResourceTags
### Properties
### Additional Properties
* **Additional Properties Type**: string

