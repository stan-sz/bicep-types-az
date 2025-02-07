# Microsoft.ContainerRegistry @ 2017-06-01-preview

## Resource Microsoft.ContainerRegistry/registries@2017-06-01-preview
* **Valid Scope(s)**: ResourceGroup
### Properties
* **apiVersion**: '2017-06-01-preview' (ReadOnly, DeployTimeConstant): The resource api version
* **id**: string (ReadOnly, DeployTimeConstant): The resource id
* **location**: string (Required): The location of the resource. This cannot be changed after the resource is created.
* **name**: string (Required, DeployTimeConstant): The resource name
* **properties**: [RegistryProperties](#registryproperties): The properties of a container registry.
* **sku**: [Sku](#sku) (Required): The SKU of a container registry.
* **tags**: [ResourceTags](#resourcetags): The tags of the resource.
* **type**: 'Microsoft.ContainerRegistry/registries' (ReadOnly, DeployTimeConstant): The resource type

## Resource Microsoft.ContainerRegistry/registries/replications@2017-06-01-preview
* **Valid Scope(s)**: ResourceGroup
### Properties
* **apiVersion**: '2017-06-01-preview' (ReadOnly, DeployTimeConstant): The resource api version
* **id**: string (ReadOnly, DeployTimeConstant): The resource id
* **location**: string (Required): The location of the resource. This cannot be changed after the resource is created.
* **name**: string (Required, DeployTimeConstant): The resource name
* **properties**: [ReplicationProperties](#replicationproperties): The properties of a replication.
* **tags**: [ResourceTags](#resourcetags): The tags of the resource.
* **type**: 'Microsoft.ContainerRegistry/registries/replications' (ReadOnly, DeployTimeConstant): The resource type

## Resource Microsoft.ContainerRegistry/registries/webhooks@2017-06-01-preview
* **Valid Scope(s)**: ResourceGroup
### Properties
* **apiVersion**: '2017-06-01-preview' (ReadOnly, DeployTimeConstant): The resource api version
* **id**: string (ReadOnly, DeployTimeConstant): The resource id
* **location**: string (Required): The location of the webhook. This cannot be changed after the resource is created.
* **name**: string (Required, DeployTimeConstant): The resource name
* **properties**: [WebhookPropertiesCreateParameters](#webhookpropertiescreateparameters): The parameters for creating the properties of a webhook.
* **tags**: [WebhookCreateParametersTags](#webhookcreateparameterstags): The tags for the webhook.
* **type**: 'Microsoft.ContainerRegistry/registries/webhooks' (ReadOnly, DeployTimeConstant): The resource type

## Function listCredentials (Microsoft.ContainerRegistry/registries@2017-06-01-preview)
* **Resource**: Microsoft.ContainerRegistry/registries
* **ApiVersion**: 2017-06-01-preview
* **Output**: [RegistryListCredentialsResult](#registrylistcredentialsresult)

## Function listEvents (Microsoft.ContainerRegistry/registries/webhooks@2017-06-01-preview)
* **Resource**: Microsoft.ContainerRegistry/registries/webhooks
* **ApiVersion**: 2017-06-01-preview
* **Output**: [EventListResult](#eventlistresult)

## RegistryProperties
### Properties
* **adminUserEnabled**: bool: The value that indicates whether the admin user is enabled.
* **creationDate**: string (ReadOnly): The creation date of the container registry in ISO8601 format.
* **loginServer**: string (ReadOnly): The URL that can be used to log into the container registry.
* **provisioningState**: 'Canceled' | 'Creating' | 'Deleting' | 'Failed' | 'Succeeded' | 'Updating' (ReadOnly): The provisioning state of the container registry at the time the operation was called.
* **status**: [Status](#status) (ReadOnly): The status of an Azure resource at the time the operation was called.
* **storageAccount**: [StorageAccountProperties](#storageaccountproperties): The properties of a storage account for a container registry. Only applicable to Basic SKU.

## Status
### Properties
* **displayStatus**: string (ReadOnly): The short label for the status.
* **message**: string (ReadOnly): The detailed message for the status, including alerts and error messages.
* **timestamp**: string (ReadOnly): The timestamp when the status was changed to the current value.

## StorageAccountProperties
### Properties
* **id**: string (Required): The resource ID of the storage account.

## Sku
### Properties
* **name**: 'Basic' | 'Managed_Basic' | 'Managed_Premium' | 'Managed_Standard' (Required): The SKU name of the container registry. Required for registry creation.
* **tier**: 'Basic' | 'Managed' (ReadOnly): The SKU tier based on the SKU name.

## ResourceTags
### Properties
### Additional Properties
* **Additional Properties Type**: string

## ReplicationProperties
### Properties
* **provisioningState**: 'Canceled' | 'Creating' | 'Deleting' | 'Failed' | 'Succeeded' | 'Updating' (ReadOnly): The provisioning state of the container registry at the time the operation was called.
* **status**: [Status](#status) (ReadOnly): The status of an Azure resource at the time the operation was called.

## ResourceTags
### Properties
### Additional Properties
* **Additional Properties Type**: string

## WebhookPropertiesCreateParameters
### Properties
* **actions**: 'delete' | 'push'[] (Required): The list of actions that trigger the webhook to post notifications.
* **customHeaders**: [WebhookPropertiesCreateParametersCustomHeaders](#webhookpropertiescreateparameterscustomheaders) (WriteOnly): Custom headers that will be added to the webhook notifications.
* **provisioningState**: 'Canceled' | 'Creating' | 'Deleting' | 'Failed' | 'Succeeded' | 'Updating' (ReadOnly): The provisioning state of the container registry at the time the operation was called.
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
* **repository**: string (ReadOnly): The repository name.
* **size**: int (ReadOnly): The number of bytes of the content. Same as Length field.
* **tag**: string (ReadOnly): The tag name.
* **url**: string (ReadOnly): The direct URL to the content.

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

