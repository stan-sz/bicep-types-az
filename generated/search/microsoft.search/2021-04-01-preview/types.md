# Microsoft.Search @ 2021-04-01-preview

## Resource Microsoft.Search/searchServices@2021-04-01-preview
* **Valid Scope(s)**: ResourceGroup
### Properties
* **apiVersion**: '2021-04-01-preview' (ReadOnly, DeployTimeConstant): The resource api version
* **id**: string (ReadOnly, DeployTimeConstant): The resource id
* **identity**: [Identity](#identity): Details about the search service identity. A null value indicates that the search service has no identity assigned.
* **location**: string (Required): The geo-location where the resource lives
* **name**: string (Required, DeployTimeConstant): The resource name
* **properties**: [SearchServiceProperties](#searchserviceproperties): Properties of the search service.
* **sku**: [Sku](#sku): Defines the SKU of an Azure Cognitive Search Service, which determines price tier and capacity limits.
* **tags**: [TrackedResourceTags](#trackedresourcetags): Resource tags.
* **type**: 'Microsoft.Search/searchServices' (ReadOnly, DeployTimeConstant): The resource type

## Resource Microsoft.Search/searchServices/privateEndpointConnections@2021-04-01-preview
* **Valid Scope(s)**: ResourceGroup
### Properties
* **apiVersion**: '2021-04-01-preview' (ReadOnly, DeployTimeConstant): The resource api version
* **id**: string (ReadOnly, DeployTimeConstant): The resource id
* **name**: string (Required, DeployTimeConstant): The resource name
* **properties**: [PrivateEndpointConnectionProperties](#privateendpointconnectionproperties): Describes the properties of an existing Private Endpoint connection to the Azure Cognitive Search service.
* **type**: 'Microsoft.Search/searchServices/privateEndpointConnections' (ReadOnly, DeployTimeConstant): The resource type

## Resource Microsoft.Search/searchServices/sharedPrivateLinkResources@2021-04-01-preview
* **Valid Scope(s)**: ResourceGroup
### Properties
* **apiVersion**: '2021-04-01-preview' (ReadOnly, DeployTimeConstant): The resource api version
* **id**: string (ReadOnly, DeployTimeConstant): The resource id
* **name**: string (Required, DeployTimeConstant): The resource name
* **properties**: [SharedPrivateLinkResourceProperties](#sharedprivatelinkresourceproperties): Describes the properties of an existing Shared Private Link Resource managed by the Azure Cognitive Search service.
* **type**: 'Microsoft.Search/searchServices/sharedPrivateLinkResources' (ReadOnly, DeployTimeConstant): The resource type

## Function listAdminKeys (Microsoft.Search/searchServices@2021-04-01-preview)
* **Resource**: Microsoft.Search/searchServices
* **ApiVersion**: 2021-04-01-preview
* **Output**: [AdminKeyResult](#adminkeyresult)

## Function listQueryKeys (Microsoft.Search/searchServices@2021-04-01-preview)
* **Resource**: Microsoft.Search/searchServices
* **ApiVersion**: 2021-04-01-preview
* **Output**: [ListQueryKeysResult](#listquerykeysresult)

## Identity
### Properties
* **principalId**: string (ReadOnly): The principal ID of the system-assigned identity of the search service.
* **tenantId**: string (ReadOnly): The tenant ID of the system-assigned identity of the search service.
* **type**: 'None' | 'SystemAssigned' | 'SystemAssigned, UserAssigned' | 'UserAssigned' (Required): The type of identity used for the resource. The type 'SystemAssigned, UserAssigned' includes both an identity created by the system and a set of user assigned identities. The type 'None' will remove all identities from the service.
* **userAssignedIdentities**: [UserAssignedManagedIdentities](#userassignedmanagedidentities): The list of user identities associated with the search service. The user identity dictionary key references will be ARM resource ids in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/userAssignedIdentities/{identityName}'.

## UserAssignedManagedIdentities
### Properties
### Additional Properties
* **Additional Properties Type**: [UserAssignedManagedIdentity](#userassignedmanagedidentity)

## UserAssignedManagedIdentity
### Properties
* **clientId**: string (ReadOnly): The client ID of user assigned identity.
* **principalId**: string (ReadOnly): The principal ID of user assigned identity.

## SearchServiceProperties
### Properties
* **authOptions**: [DataPlaneAuthOptions](#dataplaneauthoptions): Defines the options for how the data plane API of a Search service authenticates requests. This cannot be set if 'disableLocalAuth' is set to true.
* **disabledDataExfiltrationOptions**: 'All'[]: A list of data exfiltration scenarios that are explicitly disallowed for the search service. Currently, the only supported value is 'All' to disable all possible data export scenarios with more fine grained controls planned for the future.
* **disableLocalAuth**: bool: When set to true, calls to the search service will not be permitted to utilize API keys for authentication. This cannot be set to true if 'dataPlaneAuthOptions' are defined.
* **encryptionWithCmk**: [EncryptionWithCmk](#encryptionwithcmk): Describes a policy that determines how resources within the search service are to be encrypted with Customer Managed Keys.
* **eTag**: string (ReadOnly): A system generated property representing the service's etag that can be for optimistic concurrency control during updates.
* **hostingMode**: 'default' | 'highDensity': Applicable only for the standard3 SKU. You can set this property to enable up to 3 high density partitions that allow up to 1000 indexes, which is much higher than the maximum indexes allowed for any other SKU. For the standard3 SKU, the value is either 'default' or 'highDensity'. For all other SKUs, this value must be 'default'.
* **networkRuleSet**: [NetworkRuleSet](#networkruleset): Network specific rules that determine how the Azure Cognitive Search service may be reached.
* **partitionCount**: int: The number of partitions in the search service; if specified, it can be 1, 2, 3, 4, 6, or 12. Values greater than 1 are only valid for standard SKUs. For 'standard3' services with hostingMode set to 'highDensity', the allowed values are between 1 and 3.
* **privateEndpointConnections**: [PrivateEndpointConnection](#privateendpointconnection)[] (ReadOnly): The list of private endpoint connections to the Azure Cognitive Search service.
* **provisioningState**: 'failed' | 'provisioning' | 'succeeded' (ReadOnly): The state of the last provisioning operation performed on the search service. Provisioning is an intermediate state that occurs while service capacity is being established. After capacity is set up, provisioningState changes to either 'succeeded' or 'failed'. Client applications can poll provisioning status (the recommended polling interval is from 30 seconds to one minute) by using the Get Search Service operation to see when an operation is completed. If you are using the free service, this value tends to come back as 'succeeded' directly in the call to Create search service. This is because the free service uses capacity that is already set up.
* **publicNetworkAccess**: 'disabled' | 'enabled': This value can be set to 'enabled' to avoid breaking changes on existing customer resources and templates. If set to 'disabled', traffic over public interface is not allowed, and private endpoint connections would be the exclusive access method.
* **replicaCount**: int: The number of replicas in the search service. If specified, it must be a value between 1 and 12 inclusive for standard SKUs or between 1 and 3 inclusive for basic SKU.
* **semanticSearch**: 'disabled' | 'free' | 'standard': Sets options that control the availability of semantic search. This configuration is only possible for certain Azure Cognitive Search SKUs in certain locations.
* **sharedPrivateLinkResources**: [SharedPrivateLinkResource](#sharedprivatelinkresource)[] (ReadOnly): The list of shared private link resources managed by the Azure Cognitive Search service.
* **status**: 'degraded' | 'deleting' | 'disabled' | 'error' | 'provisioning' | 'running' | 'stopped' (ReadOnly): The status of the search service. Possible values include: 'running': The search service is running and no provisioning operations are underway. 'provisioning': The search service is being provisioned or scaled up or down. 'deleting': The search service is being deleted. 'degraded': The search service is degraded. This can occur when the underlying search units are not healthy. The search service is most likely operational, but performance might be slow and some requests might be dropped. 'disabled': The search service is disabled. In this state, the service will reject all API requests. 'error': The search service is in an error state. 'stopped': The search service is in a subscription that's disabled. If your service is in the degraded, disabled, or error states, it means the Azure Cognitive Search team is actively investigating the underlying issue. Dedicated services in these states are still chargeable based on the number of search units provisioned.
* **statusDetails**: string (ReadOnly): The details of the search service status.

## DataPlaneAuthOptions
### Properties
* **aadOrApiKey**: [DataPlaneAadOrApiKeyAuthOption](#dataplaneaadorapikeyauthoption): Indicates that either the API key or an access token from Azure Active Directory can be used for authentication.
* **apiKeyOnly**: any: Any object

## DataPlaneAadOrApiKeyAuthOption
### Properties
* **aadAuthFailureMode**: 'http401WithBearerChallenge' | 'http403': Describes what response the data plane API of a Search service would send for requests that failed authentication.

## EncryptionWithCmk
### Properties
* **encryptionComplianceStatus**: 'Compliant' | 'NonCompliant' (ReadOnly): Describes whether the search service is compliant or not with respect to having non customer encrypted resources. If a service has more than one non customer encrypted resource and 'Enforcement' is 'enabled' then the service will be marked as 'nonCompliant'.
* **enforcement**: 'Disabled' | 'Enabled' | 'Unspecified': Describes how a search service should enforce having one or more non customer encrypted resources.

## NetworkRuleSet
### Properties
* **bypass**: 'None': A specific data exfiltration scenario that is disabled for the service.
* **ipRules**: [IpRule](#iprule)[]: A list of IP restriction rules that defines the inbound network(s) with allowing access to the search service endpoint. At the meantime, all other public IP networks are blocked by the firewall. These restriction rules are applied only when the 'publicNetworkAccess' of the search service is 'enabled'; otherwise, traffic over public interface is not allowed even with any public IP rules, and private endpoint connections would be the exclusive access method.

## IpRule
### Properties
* **value**: string: Value corresponding to a single IPv4 address (eg., 123.1.2.3) or an IP range in CIDR format (eg., 123.1.2.3/24) to be allowed.

## PrivateEndpointConnection
### Properties
* **id**: string (ReadOnly): Fully qualified resource ID for the resource. Ex - /subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/{resourceProviderNamespace}/{resourceType}/{resourceName}
* **name**: string (ReadOnly): The name of the resource
* **properties**: [PrivateEndpointConnectionProperties](#privateendpointconnectionproperties): Describes the properties of an existing Private Endpoint connection to the Azure Cognitive Search service.
* **type**: string (ReadOnly): The type of the resource. E.g. "Microsoft.Compute/virtualMachines" or "Microsoft.Storage/storageAccounts"

## PrivateEndpointConnectionProperties
### Properties
* **privateEndpoint**: [PrivateEndpointConnectionPropertiesPrivateEndpoint](#privateendpointconnectionpropertiesprivateendpoint): The private endpoint resource from Microsoft.Network provider.
* **privateLinkServiceConnectionState**: [PrivateEndpointConnectionPropertiesPrivateLinkServiceConnectionState](#privateendpointconnectionpropertiesprivatelinkserviceconnectionstate): Describes the current state of an existing Private Link Service connection to the Azure Private Endpoint.

## PrivateEndpointConnectionPropertiesPrivateEndpoint
### Properties
* **id**: string: The resource id of the private endpoint resource from Microsoft.Network provider.

## PrivateEndpointConnectionPropertiesPrivateLinkServiceConnectionState
### Properties
* **actionsRequired**: string: A description of any extra actions that may be required.
* **description**: string: The description for the private link service connection state.
* **status**: 'Approved' | 'Disconnected' | 'Pending' | 'Rejected': Status of the the private link service connection. Can be Pending, Approved, Rejected, or Disconnected.

## SharedPrivateLinkResource
### Properties
* **id**: string (ReadOnly): Fully qualified resource ID for the resource. Ex - /subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/{resourceProviderNamespace}/{resourceType}/{resourceName}
* **name**: string (ReadOnly): The name of the resource
* **properties**: [SharedPrivateLinkResourceProperties](#sharedprivatelinkresourceproperties): Describes the properties of an existing Shared Private Link Resource managed by the Azure Cognitive Search service.
* **type**: string (ReadOnly): The type of the resource. E.g. "Microsoft.Compute/virtualMachines" or "Microsoft.Storage/storageAccounts"

## SharedPrivateLinkResourceProperties
### Properties
* **groupId**: string: The group id from the provider of resource the shared private link resource is for.
* **privateLinkResourceId**: string: The resource id of the resource the shared private link resource is for.
* **provisioningState**: 'Deleting' | 'Failed' | 'Incomplete' | 'Succeeded' | 'Updating': The provisioning state of the shared private link resource. Can be Updating, Deleting, Failed, Succeeded, Incomplete or other yet to be documented value.
* **requestMessage**: string: The request message for requesting approval of the shared private link resource.
* **resourceRegion**: string: Optional. Can be used to specify the Azure Resource Manager location of the resource to which a shared private link is to be created. This is only required for those resources whose DNS configuration are regional (such as Azure Kubernetes Service).
* **status**: 'Approved' | 'Disconnected' | 'Pending' | 'Rejected': Status of the shared private link resource. Can be Pending, Approved, Rejected, Disconnected or other yet to be documented value.

## Sku
### Properties
* **name**: 'basic' | 'free' | 'standard' | 'standard2' | 'standard3' | 'storage_optimized_l1' | 'storage_optimized_l2': The SKU of the search service. Valid values include: 'free': Shared service. 'basic': Dedicated service with up to 3 replicas. 'standard': Dedicated service with up to 12 partitions and 12 replicas. 'standard2': Similar to standard, but with more capacity per search unit. 'standard3': The largest Standard offering with up to 12 partitions and 12 replicas (or up to 3 partitions with more indexes if you also set the hostingMode property to 'highDensity'). 'storage_optimized_l1': Supports 1TB per partition, up to 12 partitions. 'storage_optimized_l2': Supports 2TB per partition, up to 12 partitions.'

## TrackedResourceTags
### Properties
### Additional Properties
* **Additional Properties Type**: string

## AdminKeyResult
### Properties
* **primaryKey**: string (ReadOnly): The primary admin API key of the search service.
* **secondaryKey**: string (ReadOnly): The secondary admin API key of the search service.

## ListQueryKeysResult
### Properties
* **nextLink**: string (ReadOnly): Request URL that can be used to query next page of query keys. Returned when the total number of requested query keys exceed maximum page size.
* **value**: [QueryKey](#querykey)[] (ReadOnly): The query keys for the Azure Cognitive Search service.

## QueryKey
### Properties
* **key**: string (ReadOnly): The value of the query API key.
* **name**: string (ReadOnly): The name of the query API key; may be empty.

