# Microsoft.ContainerRegistry @ 2021-09-01

## Resource Microsoft.ContainerRegistry/registries@2021-09-01
* **Valid Scope(s)**: ResourceGroup
### Properties
* **apiVersion**: '2021-09-01' (ReadOnly, DeployTimeConstant): The resource api version
* **id**: string (ReadOnly, DeployTimeConstant): The resource id
* **identity**: [IdentityProperties](#identityproperties): Managed identity for the resource.
* **location**: string (Required): The location of the resource. This cannot be changed after the resource is created.
* **name**: string (Required, DeployTimeConstant): The resource name
* **properties**: [RegistryProperties](#registryproperties): The properties of a container registry.
* **sku**: [Sku](#sku) (Required): The SKU of a container registry.
* **systemData**: [SystemData](#systemdata) (ReadOnly): Metadata pertaining to creation and last modification of the resource.
* **tags**: [ResourceTags](#resourcetags): The tags of the resource.
* **type**: 'Microsoft.ContainerRegistry/registries' (ReadOnly, DeployTimeConstant): The resource type

## Resource Microsoft.ContainerRegistry/registries/privateEndpointConnections@2021-09-01
* **Valid Scope(s)**: ResourceGroup
### Properties
* **apiVersion**: '2021-09-01' (ReadOnly, DeployTimeConstant): The resource api version
* **id**: string (ReadOnly, DeployTimeConstant): The resource id
* **name**: string (Required, DeployTimeConstant): The resource name
* **properties**: [PrivateEndpointConnectionProperties](#privateendpointconnectionproperties): The properties of a private endpoint connection.
* **systemData**: [SystemData](#systemdata) (ReadOnly): Metadata pertaining to creation and last modification of the resource.
* **type**: 'Microsoft.ContainerRegistry/registries/privateEndpointConnections' (ReadOnly, DeployTimeConstant): The resource type

## Resource Microsoft.ContainerRegistry/registries/replications@2021-09-01
* **Valid Scope(s)**: ResourceGroup
### Properties
* **apiVersion**: '2021-09-01' (ReadOnly, DeployTimeConstant): The resource api version
* **id**: string (ReadOnly, DeployTimeConstant): The resource id
* **location**: string (Required): The location of the resource. This cannot be changed after the resource is created.
* **name**: string (Required, DeployTimeConstant): The resource name
* **properties**: [ReplicationProperties](#replicationproperties): The properties of a replication.
* **systemData**: [SystemData](#systemdata) (ReadOnly): Metadata pertaining to creation and last modification of the resource.
* **tags**: [ResourceTags](#resourcetags): The tags of the resource.
* **type**: 'Microsoft.ContainerRegistry/registries/replications' (ReadOnly, DeployTimeConstant): The resource type

## Resource Microsoft.ContainerRegistry/registries/webhooks@2021-09-01
* **Valid Scope(s)**: ResourceGroup
### Properties
* **apiVersion**: '2021-09-01' (ReadOnly, DeployTimeConstant): The resource api version
* **id**: string (ReadOnly, DeployTimeConstant): The resource id
* **location**: string (Required): The location of the webhook. This cannot be changed after the resource is created.
* **name**: string (Required, DeployTimeConstant): The resource name
* **properties**: [WebhookPropertiesCreateParameters](#webhookpropertiescreateparameters): The parameters for creating the properties of a webhook.
* **systemData**: [SystemData](#systemdata) (ReadOnly): Metadata pertaining to creation and last modification of the resource.
* **tags**: [WebhookCreateParametersTags](#webhookcreateparameterstags): The tags for the webhook.
* **type**: 'Microsoft.ContainerRegistry/registries/webhooks' (ReadOnly, DeployTimeConstant): The resource type

## Function listCredentials (Microsoft.ContainerRegistry/registries@2021-09-01)
* **Resource**: Microsoft.ContainerRegistry/registries
* **ApiVersion**: 2021-09-01
* **Output**: [RegistryListCredentialsResult](#registrylistcredentialsresult)

## Function listEvents (Microsoft.ContainerRegistry/registries/webhooks@2021-09-01)
* **Resource**: Microsoft.ContainerRegistry/registries/webhooks
* **ApiVersion**: 2021-09-01
* **Output**: [EventListResult](#eventlistresult)

## IdentityProperties
### Properties
* **principalId**: string: The principal ID of resource identity.
* **tenantId**: string: The tenant ID of resource.
* **type**: 'None' | 'SystemAssigned' | 'SystemAssigned, UserAssigned' | 'UserAssigned': The identity type.
* **userAssignedIdentities**: [IdentityPropertiesUserAssignedIdentities](#identitypropertiesuserassignedidentities): The list of user identities associated with the resource. The user identity 
dictionary key references will be ARM resource ids in the form: 
'/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/
    providers/Microsoft.ManagedIdentity/userAssignedIdentities/{identityName}'.

## IdentityPropertiesUserAssignedIdentities
### Properties
### Additional Properties
* **Additional Properties Type**: [UserIdentityProperties](#useridentityproperties)

## UserIdentityProperties
### Properties
* **clientId**: string: The client id of user assigned identity.
* **principalId**: string: The principal id of user assigned identity.

## RegistryProperties
### Properties
* **adminUserEnabled**: bool: The value that indicates whether the admin user is enabled.
* **creationDate**: string (ReadOnly): The creation date of the container registry in ISO8601 format.
* **dataEndpointEnabled**: bool: Enable a single data endpoint per region for serving data.
* **dataEndpointHostNames**: string[] (ReadOnly): List of host names that will serve data when dataEndpointEnabled is true.
* **encryption**: [EncryptionProperty](#encryptionproperty)
* **loginServer**: string (ReadOnly): The URL that can be used to log into the container registry.
* **networkRuleBypassOptions**: 'AzureServices' | 'None': Whether to allow trusted Azure services to access a network restricted registry.
* **networkRuleSet**: [NetworkRuleSet](#networkruleset): The network rule set for a container registry.
* **policies**: [Policies](#policies): The policies for a container registry.
* **privateEndpointConnections**: [PrivateEndpointConnection](#privateendpointconnection)[] (ReadOnly): List of private endpoint connections for a container registry.
* **provisioningState**: 'Canceled' | 'Creating' | 'Deleting' | 'Failed' | 'Succeeded' | 'Updating' (ReadOnly): The provisioning state of private endpoint connection resource.
* **publicNetworkAccess**: 'Disabled' | 'Enabled': Whether or not public network access is allowed for the container registry.
* **status**: [Status](#status) (ReadOnly): The status of an Azure resource at the time the operation was called.
* **zoneRedundancy**: 'Disabled' | 'Enabled': Whether or not zone redundancy is enabled for this container registry

## EncryptionProperty
### Properties
* **keyVaultProperties**: [KeyVaultProperties](#keyvaultproperties)
* **status**: 'disabled' | 'enabled': Indicates whether or not the encryption is enabled for container registry.

## KeyVaultProperties
### Properties
* **identity**: string: The client id of the identity which will be used to access key vault.
* **keyIdentifier**: string: Key vault uri to access the encryption key.
* **keyRotationEnabled**: bool (ReadOnly): Auto key rotation status for a CMK enabled registry.
* **lastKeyRotationTimestamp**: string (ReadOnly): Timestamp of the last successful key rotation.
* **versionedKeyIdentifier**: string (ReadOnly): The fully qualified key identifier that includes the version of the key that is actually used for encryption.

## NetworkRuleSet
### Properties
* **defaultAction**: 'Allow' | 'Deny' (Required): The default action of allow or deny when no other rules match.
* **ipRules**: [IPRule](#iprule)[]: The IP ACL rules.

## IPRule
### Properties
* **action**: 'Allow': The action of IP ACL rule.
* **value**: string (Required): Specifies the IP or IP range in CIDR format. Only IPV4 address is allowed.

## Policies
### Properties
* **exportPolicy**: [ExportPolicy](#exportpolicy): The export policy for a container registry.
* **quarantinePolicy**: [QuarantinePolicy](#quarantinepolicy): The quarantine policy for a container registry.
* **retentionPolicy**: [RetentionPolicy](#retentionpolicy): The retention policy for a container registry.
* **trustPolicy**: [TrustPolicy](#trustpolicy): The content trust policy for a container registry.

## ExportPolicy
### Properties
* **status**: 'disabled' | 'enabled': The value that indicates whether the policy is enabled or not.

## QuarantinePolicy
### Properties
* **status**: 'disabled' | 'enabled': The value that indicates whether the policy is enabled or not.

## RetentionPolicy
### Properties
* **days**: int: The number of days to retain an untagged manifest after which it gets purged.
* **lastUpdatedTime**: string (ReadOnly): The timestamp when the policy was last updated.
* **status**: 'disabled' | 'enabled': The value that indicates whether the policy is enabled or not.

## TrustPolicy
### Properties
* **status**: 'disabled' | 'enabled': The value that indicates whether the policy is enabled or not.
* **type**: 'Notary': The type of trust policy.

## PrivateEndpointConnection
### Properties
* **id**: string (ReadOnly): The resource ID.
* **name**: string (ReadOnly): The name of the resource.
* **properties**: [PrivateEndpointConnectionProperties](#privateendpointconnectionproperties): The properties of a private endpoint connection.
* **systemData**: [SystemData](#systemdata) (ReadOnly): Metadata pertaining to creation and last modification of the resource.
* **type**: string (ReadOnly): The type of the resource.

## PrivateEndpointConnectionProperties
### Properties
* **privateEndpoint**: [PrivateEndpoint](#privateendpoint): The Private Endpoint resource.
* **privateLinkServiceConnectionState**: [PrivateLinkServiceConnectionState](#privatelinkserviceconnectionstate): The state of a private link service connection.
* **provisioningState**: 'Canceled' | 'Creating' | 'Deleting' | 'Failed' | 'Succeeded' | 'Updating' (ReadOnly): The provisioning state of private endpoint connection resource.

## PrivateEndpoint
### Properties
* **id**: string: This is private endpoint resource created with Microsoft.Network resource provider.

## PrivateLinkServiceConnectionState
### Properties
* **actionsRequired**: 'None' | 'Recreate': A message indicating if changes on the service provider require any updates on the consumer.
* **description**: string: The description for connection status. For example if connection is rejected it can indicate reason for rejection.
* **status**: 'Approved' | 'Disconnected' | 'Pending' | 'Rejected': The private link service connection status.

## SystemData
### Properties
* **createdAt**: string: The timestamp of resource creation (UTC).
* **createdBy**: string: The identity that created the resource.
* **createdByType**: 'Application' | 'Key' | 'ManagedIdentity' | 'User': The type of identity that created the resource.
* **lastModifiedAt**: string: The timestamp of resource modification (UTC).
* **lastModifiedBy**: string: The identity that last modified the resource.
* **lastModifiedByType**: 'Application' | 'Key' | 'ManagedIdentity' | 'User': The type of identity that last modified the resource.

## Status
### Properties
* **displayStatus**: string (ReadOnly): The short label for the status.
* **message**: string (ReadOnly): The detailed message for the status, including alerts and error messages.
* **timestamp**: string (ReadOnly): The timestamp when the status was changed to the current value.

## Sku
### Properties
* **name**: 'Basic' | 'Classic' | 'Premium' | 'Standard' (Required): The SKU name of the container registry. Required for registry creation.
* **tier**: 'Basic' | 'Classic' | 'Premium' | 'Standard' (ReadOnly): The SKU tier based on the SKU name.

## ResourceTags
### Properties
### Additional Properties
* **Additional Properties Type**: string

## ReplicationProperties
### Properties
* **provisioningState**: 'Canceled' | 'Creating' | 'Deleting' | 'Failed' | 'Succeeded' | 'Updating' (ReadOnly): The provisioning state of private endpoint connection resource.
* **regionEndpointEnabled**: bool: Specifies whether the replication's regional endpoint is enabled. Requests will not be routed to a replication whose regional endpoint is disabled, however its data will continue to be synced with other replications.
* **status**: [Status](#status) (ReadOnly): The status of an Azure resource at the time the operation was called.
* **zoneRedundancy**: 'Disabled' | 'Enabled': Whether or not zone redundancy is enabled for this container registry

## ResourceTags
### Properties
### Additional Properties
* **Additional Properties Type**: string

## WebhookPropertiesCreateParameters
### Properties
* **actions**: 'chart_delete' | 'chart_push' | 'delete' | 'push' | 'quarantine'[] (Required): The list of actions that trigger the webhook to post notifications.
* **customHeaders**: [WebhookPropertiesCreateParametersCustomHeaders](#webhookpropertiescreateparameterscustomheaders) (WriteOnly): Custom headers that will be added to the webhook notifications.
* **provisioningState**: 'Canceled' | 'Creating' | 'Deleting' | 'Failed' | 'Succeeded' | 'Updating' (ReadOnly): The provisioning state of private endpoint connection resource.
* **scope**: string: The scope of repositories where the event can be triggered. For example, 'foo:*' means events for all tags under repository 'foo'. 'foo:bar' means events for 'foo:bar' only. 'foo' is equivalent to 'foo:latest'. Empty means all events.
* **serviceUri**: string (Required, WriteOnly): The service URI for the webhook to post notifications.
* **status**: 'disabled' | 'enabled': The status of the webhook at the time the operation was called.

## WebhookPropertiesCreateParametersCustomHeaders
### Properties
### Additional Properties
* **Additional Properties Type**: string

## WebhookCreateParametersTags
### Properties
### Additional Properties
* **Additional Properties Type**: string

## RegistryListCredentialsResult
### Properties
* **passwords**: [RegistryPassword](#registrypassword)[] (ReadOnly): The list of passwords for a container registry.
* **username**: string (ReadOnly): The username for a container registry.

## RegistryPassword
### Properties
* **name**: 'password' | 'password2' (ReadOnly): The password name.
* **value**: string (ReadOnly): The password value.

## EventListResult
### Properties
* **nextLink**: string (ReadOnly): The URI that can be used to request the next list of events.
* **value**: [Event](#event)[] (ReadOnly): The list of events. Since this list may be incomplete, the nextLink field should be used to request the next list of events.

## Event
### Properties
* **eventRequestMessage**: [EventRequestMessage](#eventrequestmessage) (ReadOnly): The event request message sent to the service URI.
* **eventResponseMessage**: [EventResponseMessage](#eventresponsemessage) (ReadOnly): The event response message received from the service URI.
* **id**: string (ReadOnly): The event ID.

## EventRequestMessage
### Properties
* **content**: [EventContent](#eventcontent) (ReadOnly): The content of the event request message.
* **headers**: [EventRequestMessageHeaders](#eventrequestmessageheaders) (ReadOnly): The headers of the event request message.
* **method**: string (ReadOnly): The HTTP method used to send the event request message.
* **requestUri**: string (ReadOnly): The URI used to send the event request message.
* **version**: string (ReadOnly): The HTTP message version.

## EventContent
### Properties
* **action**: string (ReadOnly): The action that encompasses the provided event.
* **actor**: [Actor](#actor) (ReadOnly): The agent that initiated the event. For most situations, this could be from the authorization context of the request.
* **id**: string (ReadOnly): The event ID.
* **request**: [Request](#request) (ReadOnly): The request that generated the event.
* **source**: [Source](#source) (ReadOnly): The registry node that generated the event. Put differently, while the actor initiates the event, the source generates it.
* **target**: [Target](#target) (ReadOnly): The target of the event.
* **timestamp**: string (ReadOnly): The time at which the event occurred.

## Actor
### Properties
* **name**: string (ReadOnly): The subject or username associated with the request context that generated the event.

## Request
### Properties
* **addr**: string (ReadOnly): The IP or hostname and possibly port of the client connection that initiated the event. This is the RemoteAddr from the standard http request.
* **host**: string (ReadOnly): The externally accessible hostname of the registry instance, as specified by the http host header on incoming requests.
* **id**: string (ReadOnly): The ID of the request that initiated the event.
* **method**: string (ReadOnly): The request method that generated the event.
* **useragent**: string (ReadOnly): The user agent header of the request.

## Source
### Properties
* **addr**: string (ReadOnly): The IP or hostname and the port of the registry node that generated the event. Generally, this will be resolved by os.Hostname() along with the running port.
* **instanceID**: string (ReadOnly): The running instance of an application. Changes after each restart.

## Target
### Properties
* **digest**: string (ReadOnly): The digest of the content, as defined by the Registry V2 HTTP API Specification.
* **length**: int (ReadOnly): The number of bytes of the content. Same as Size field.
* **mediaType**: string (ReadOnly): The MIME type of the referenced object.
* **name**: string (ReadOnly): The name of the artifact.
* **repository**: string (ReadOnly): The repository name.
* **size**: int (ReadOnly): The number of bytes of the content. Same as Length field.
* **tag**: string (ReadOnly): The tag name.
* **url**: string (ReadOnly): The direct URL to the content.
* **version**: string (ReadOnly): The version of the artifact.

## EventRequestMessageHeaders
### Properties
### Additional Properties
* **Additional Properties Type**: string

## EventResponseMessage
### Properties
* **content**: string (ReadOnly): The content of the event response message.
* **headers**: [EventResponseMessageHeaders](#eventresponsemessageheaders) (ReadOnly): The headers of the event response message.
* **reasonPhrase**: string (ReadOnly): The reason phrase of the event response message.
* **statusCode**: string (ReadOnly): The status code of the event response message.
* **version**: string (ReadOnly): The HTTP message version.

## EventResponseMessageHeaders
### Properties
### Additional Properties
* **Additional Properties Type**: string

