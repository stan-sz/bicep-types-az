# Microsoft.Web @ 2015-08-01-preview

## Resource Microsoft.Web/connections@2015-08-01-preview
* **Valid Scope(s)**: ResourceGroup
### Properties
* **apiVersion**: '2015-08-01-preview' (ReadOnly, DeployTimeConstant): The resource api version
* **id**: string (ReadOnly, DeployTimeConstant): The resource id
* **kind**: string: Kind of resource
* **location**: string (Required): Resource Location
* **name**: string (Required, DeployTimeConstant): The resource name
* **properties**: [ConnectionProperties](#connectionproperties)
* **tags**: [ResourceTags](#resourcetags): Resource tags
* **type**: 'Microsoft.Web/connections' (ReadOnly, DeployTimeConstant): The resource type

## Function listConnectionKeys (Microsoft.Web/connections@2015-08-01-preview)
* **Resource**: Microsoft.Web/connections
* **ApiVersion**: 2015-08-01-preview
* **Input**: [ListConnectionKeysInput](#listconnectionkeysinput)
* **Output**: [ConnectionSecrets](#connectionsecrets)

## Function listConsentLinks (Microsoft.Web/connections@2015-08-01-preview)
* **Resource**: Microsoft.Web/connections
* **ApiVersion**: 2015-08-01-preview
* **Input**: [ConsentLinkInput](#consentlinkinput)
* **Output**: [ConsentLinkPayload](#consentlinkpayload)

## ConnectionProperties
### Properties
* **api**: [ExpandedParentApiEntity](#expandedparentapientity): expanded parent object for expansion
* **changedTime**: string: Timestamp of last connection change.
* **createdTime**: string: Timestamp of the connection creation
* **customParameterValues**: [ConnectionPropertiesCustomParameterValues](#connectionpropertiescustomparametervalues): Custom login setting values.
* **displayName**: string: display name
* **firstExpirationTime**: string: Time in UTC when the first expiration of OAuth tokens
* **keywords**: string[]: List of Keywords that tag the acl
* **metadata**: any: Any object
* **name**: string: connection name
* **nonSecretParameterValues**: [ConnectionPropertiesNonSecretParameterValues](#connectionpropertiesnonsecretparametervalues): Tokens/Claim
* **parameterValues**: [ConnectionPropertiesParameterValues](#connectionpropertiesparametervalues): Tokens/Claim
* **statuses**: [ConnectionStatus](#connectionstatus)[]: Status of the connection
* **tenantId**: string

## ExpandedParentApiEntity
### Properties
* **id**: string: Resource Id
* **kind**: string: Kind of resource
* **location**: string (Required): Resource Location
* **name**: string: Resource Name
* **properties**: [ExpandedParentApiEntityProperties](#expandedparentapientityproperties)
* **tags**: [ResourceTags](#resourcetags): Resource tags
* **type**: string: Resource type

## ExpandedParentApiEntityProperties
### Properties
* **entity**: [ResponseMessageEnvelopeApiEntity](#responsemessageenvelopeapientity): Message envelope that contains the common Azure resource manager properties and the resource provider specific content
* **id**: string: Id of connection provider

## ResponseMessageEnvelopeApiEntity
### Properties
* **id**: string: Resource Id. Typically id is populated only for responses to GET requests. Caller is responsible for passing in this
            value for GET requests only.
            For example: /subscriptions/{subscriptionId}/resourceGroups/{resourceGroupId}/providers/Microsoft.Web/sites/{sitename}
* **location**: string: Geo region resource belongs to e.g. SouthCentralUS, SouthEastAsia
* **name**: string: Name of resource
* **plan**: [ArmPlan](#armplan): The plan object in an ARM, represents a marketplace plan
* **properties**: [ApiEntity](#apientity): API Management
* **sku**: [SkuDescription](#skudescription): Describes a sku for a scalable resource
* **tags**: [ResponseMessageEnvelopeApiEntityTags](#responsemessageenvelopeapientitytags): Tags associated with resource
* **type**: string: Type of resource e.g Microsoft.Web/sites

## ArmPlan
### Properties
* **name**: string: The name
* **product**: string: The product
* **promotionCode**: string: The promotion code
* **publisher**: string: The publisher
* **version**: string: Version of product

## ApiEntity
### Properties
* **id**: string: Resource Id
* **kind**: string: Kind of resource
* **location**: string (Required): Resource Location
* **name**: string: Resource Name
* **properties**: [ApiEntityProperties](#apientityproperties)
* **tags**: [ResourceTags](#resourcetags): Resource tags
* **type**: string: Resource type

## ApiEntityProperties
### Properties
* **apiDefinitionUrl**: string: API definition Url - url where the swagger can be downloaded from
* **backendService**: [BackendServiceDefinition](#backendservicedefinition): API definitions with backend urls
* **capabilities**: string[]: Capabilities
* **changedTime**: string: Timestamp of last connection change.
* **connectionParameters**: [ApiEntityPropertiesConnectionParameters](#apientitypropertiesconnectionparameters): Connection parameters
* **createdTime**: string: Timestamp of the connection creation
* **generalInformation**: [GeneralApiInformation](#generalapiinformation): General API information
* **metadata**: any: Any object
* **name**: string: Name of the API
            the URL path of this API when exposed via APIM
* **path**: string: the URL path of this API when exposed via APIM
* **policies**: [ApiPolicies](#apipolicies): API policies
* **protocols**: string[]: Protocols supported by the front end - http/https
* **runtimeUrls**: string[]: Read only property returning the runtime endpoints where the API can be called

## BackendServiceDefinition
### Properties
* **id**: string: Resource Id
* **kind**: string: Kind of resource
* **location**: string (Required): Resource Location
* **name**: string: Resource Name
* **properties**: [BackendServiceDefinitionProperties](#backendservicedefinitionproperties)
* **tags**: [ResourceTags](#resourcetags): Resource tags
* **type**: string: Resource type

## BackendServiceDefinitionProperties
### Properties
* **hostingEnvironmentServiceUrls**: [HostingEnvironmentServiceDescriptions](#hostingenvironmentservicedescriptions)[]: Service Urls per Hosting environment
* **serviceUrl**: string: Url from which the swagger payload will be fetched

## HostingEnvironmentServiceDescriptions
### Properties
* **hostId**: string: Host Id
* **hostingEnvironmentId**: string: Hosting environment Id
* **serviceUrl**: string: service url to use
* **useInternalRouting**: bool: When the backend url is in same ASE, for performance reason this flag can be set to true
            If WebApp.DisableHostNames is also set it improves the security by making the back end accessible only 
            via API calls
            Note: calls will fail if this option is used but back end is not on the same ASE

## ResourceTags
### Properties
### Additional Properties
* **Additional Properties Type**: string

## ApiEntityPropertiesConnectionParameters
### Properties
### Additional Properties
* **Additional Properties Type**: [ConnectionParameter](#connectionparameter)

## ConnectionParameter
### Properties
* **defaultValue**: any: Any object
* **oAuthSettings**: [ApiOAuthSettings](#apioauthsettings): OAuth settings for the connection provider
* **type**: 'array' | 'bool' | 'connection' | 'int' | 'oauthSetting' | 'object' | 'secureobject' | 'securestring' | 'string': Type of the parameter
* **uiDefinition**: any: Any object

## ApiOAuthSettings
### Properties
* **clientId**: string: Resource provider client id
* **clientSecret**: string: Client Secret needed for OAuth
* **customParameters**: [ApiOAuthSettingsCustomParameters](#apioauthsettingscustomparameters): OAuth parameters key is the name of parameter
* **identityProvider**: string: Identity provider
* **properties**: any: Any object
* **redirectUrl**: string: Url
* **scopes**: string[]: OAuth scopes

## ApiOAuthSettingsCustomParameters
### Properties
### Additional Properties
* **Additional Properties Type**: [ApiOAuthSettingsParameter](#apioauthsettingsparameter)

## ApiOAuthSettingsParameter
### Properties
* **options**: any: Any object
* **uiDefinition**: any: Any object
* **value**: string: Value

## GeneralApiInformation
### Properties
* **id**: string: Resource Id
* **kind**: string: Kind of resource
* **location**: string (Required): Resource Location
* **name**: string: Resource Name
* **properties**: [GeneralApiInformationProperties](#generalapiinformationproperties)
* **tags**: [ResourceTags](#resourcetags): Resource tags
* **type**: string: Resource type

## GeneralApiInformationProperties
### Properties
* **connectionDisplayName**: string: DefaultConnectionNameTemplate
* **connectionPortalUrl**: any: Any object
* **description**: string: Description
* **displayName**: string: Display Name
* **iconUrl**: string: Icon Url
* **termsOfUseUrl**: string: a public accessible url of the Terms Of Use Url of this API

## ResourceTags
### Properties
### Additional Properties
* **Additional Properties Type**: string

## ApiPolicies
### Properties
* **id**: string: Resource Id
* **kind**: string: Kind of resource
* **location**: string (Required): Resource Location
* **name**: string: Resource Name
* **properties**: [ApiPoliciesProperties](#apipoliciesproperties)
* **tags**: [ResourceTags](#resourcetags): Resource tags
* **type**: string: Resource type

## ApiPoliciesProperties
### Properties
* **content**: string: Content of xml policy

## ResourceTags
### Properties
### Additional Properties
* **Additional Properties Type**: string

## ResourceTags
### Properties
### Additional Properties
* **Additional Properties Type**: string

## SkuDescription
### Properties
* **capacity**: int: Current number of instances assigned to the resource
* **family**: string: Family code of the resource sku
* **name**: string: Name of the resource sku
* **size**: string: Size specifier of the resource sku
* **tier**: string: Service Tier of the resource sku

## ResponseMessageEnvelopeApiEntityTags
### Properties
### Additional Properties
* **Additional Properties Type**: string

## ResourceTags
### Properties
### Additional Properties
* **Additional Properties Type**: string

## ConnectionPropertiesCustomParameterValues
### Properties
### Additional Properties
* **Additional Properties Type**: [ParameterCustomLoginSettingValues](#parametercustomloginsettingvalues)

## ParameterCustomLoginSettingValues
### Properties
* **id**: string: Resource Id
* **kind**: string: Kind of resource
* **location**: string (Required): Resource Location
* **name**: string: Resource Name
* **properties**: [ParameterCustomLoginSettingValuesProperties](#parametercustomloginsettingvaluesproperties)
* **tags**: [ResourceTags](#resourcetags): Resource tags
* **type**: string: Resource type

## ParameterCustomLoginSettingValuesProperties
### Properties
* **customParameters**: [ParameterCustomLoginSettingValuesPropertiesCustomParameters](#parametercustomloginsettingvaluespropertiescustomparameters): Custom parameters.

## ParameterCustomLoginSettingValuesPropertiesCustomParameters
### Properties
### Additional Properties
* **Additional Properties Type**: [CustomLoginSettingValue](#customloginsettingvalue)

## CustomLoginSettingValue
### Properties
* **id**: string: Resource Id
* **kind**: string: Kind of resource
* **location**: string (Required): Resource Location
* **name**: string: Resource Name
* **properties**: [CustomLoginSettingValueProperties](#customloginsettingvalueproperties)
* **tags**: [ResourceTags](#resourcetags): Resource tags
* **type**: string: Resource type

## CustomLoginSettingValueProperties
### Properties
* **option**: string: Option selected for this custom login setting value

## ResourceTags
### Properties
### Additional Properties
* **Additional Properties Type**: string

## ResourceTags
### Properties
### Additional Properties
* **Additional Properties Type**: string

## ConnectionPropertiesNonSecretParameterValues
### Properties
### Additional Properties
* **Additional Properties Type**: any

## ConnectionPropertiesParameterValues
### Properties
### Additional Properties
* **Additional Properties Type**: any

## ConnectionStatus
### Properties
* **id**: string: Resource Id
* **kind**: string: Kind of resource
* **location**: string (Required): Resource Location
* **name**: string: Resource Name
* **properties**: [ConnectionStatusProperties](#connectionstatusproperties)
* **tags**: [ResourceTags](#resourcetags): Resource tags
* **type**: string: Resource type

## ConnectionStatusProperties
### Properties
* **error**: [ConnectionError](#connectionerror): Connection error
* **status**: string: Status
* **target**: string: Target of the error

## ConnectionError
### Properties
* **id**: string: Resource Id
* **kind**: string: Kind of resource
* **location**: string (Required): Resource Location
* **name**: string: Resource Name
* **properties**: [ConnectionErrorProperties](#connectionerrorproperties)
* **tags**: [ResourceTags](#resourcetags): Resource tags
* **type**: string: Resource type

## ConnectionErrorProperties
### Properties
* **code**: string: code of the status
* **message**: string: Description of the status

## ResourceTags
### Properties
### Additional Properties
* **Additional Properties Type**: string

## ResourceTags
### Properties
### Additional Properties
* **Additional Properties Type**: string

## ResourceTags
### Properties
### Additional Properties
* **Additional Properties Type**: string

## ListConnectionKeysInput
### Properties
* **id**: string (WriteOnly): Resource Id
* **kind**: string (WriteOnly): Kind of resource
* **location**: string (Required, WriteOnly): Resource Location
* **name**: string (WriteOnly): Resource Name
* **properties**: [ListConnectionKeysInputProperties](#listconnectionkeysinputproperties) (WriteOnly)
* **tags**: [ResourceTags](#resourcetags) (WriteOnly): Resource tags
* **type**: string (WriteOnly): Resource type

## ListConnectionKeysInputProperties
### Properties
* **validityTimeSpan**: string (WriteOnly): time span for how long the keys will be valid

## ResourceTags
### Properties
### Additional Properties
* **Additional Properties Type**: string

## ConnectionSecrets
### Properties
* **connectionKey**: string (ReadOnly): Connection Key
* **parameterValues**: [ConnectionSecretsParameterValues](#connectionsecretsparametervalues) (ReadOnly): Tokens/Claim

## ConnectionSecretsParameterValues
### Properties
### Additional Properties
* **Additional Properties Type**: any

## ConsentLinkInput
### Properties
* **id**: string (WriteOnly): Resource Id
* **kind**: string (WriteOnly): Kind of resource
* **location**: string (Required, WriteOnly): Resource Location
* **name**: string (WriteOnly): Resource Name
* **properties**: [ConsentLinkInputProperties](#consentlinkinputproperties) (WriteOnly)
* **tags**: [ResourceTags](#resourcetags) (WriteOnly): Resource tags
* **type**: string (WriteOnly): Resource type

## ConsentLinkInputProperties
### Properties
* **parameters**: [ConsentLinkInputParameter](#consentlinkinputparameter)[] (WriteOnly): Array of links

## ConsentLinkInputParameter
### Properties
* **objectId**: string (WriteOnly): AAD OID (user or group) if the principal type is ActiveDirectory.
            MSA PUID if the principal type is MicrosoftAccount.
* **parameterName**: string (WriteOnly): Name of the parameter in the connection provider's oauthSettings
* **principalType**: 'ActiveDirectory' | 'Connection' | 'MicrosoftAccount' (WriteOnly): Principal type
* **redirectUrl**: string (WriteOnly): Name of the parameter in the connection provider's oauthSettings
* **tenantId**: string (WriteOnly): Tenant Id

## ResourceTags
### Properties
### Additional Properties
* **Additional Properties Type**: string

## ConsentLinkPayload
### Properties
* **value**: [ConsentLink](#consentlink)[] (ReadOnly): Collection of resources

## ConsentLink
### Properties
* **displayName**: string (ReadOnly): Display Name of the parameter in the connection provider's oauthSettings
* **firstPartyLoginUri**: string (ReadOnly): Uri for first party login
* **link**: string (ReadOnly): Uri for the consent link
* **status**: 'Authenticated' | 'Error' | 'Unauthenticated' (ReadOnly): Status of the link

