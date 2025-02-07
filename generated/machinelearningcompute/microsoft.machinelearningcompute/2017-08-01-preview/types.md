# Microsoft.MachineLearningCompute @ 2017-08-01-preview

## Resource Microsoft.MachineLearningCompute/operationalizationClusters@2017-08-01-preview
* **Valid Scope(s)**: ResourceGroup
### Properties
* **apiVersion**: '2017-08-01-preview' (ReadOnly, DeployTimeConstant): The resource api version
* **id**: string (ReadOnly, DeployTimeConstant): The resource id
* **location**: string (Required): Specifies the location of the resource.
* **name**: string (Required, DeployTimeConstant): The resource name
* **properties**: [OperationalizationClusterProperties](#operationalizationclusterproperties): Properties of an operationalization cluster
* **tags**: [ResourceTags](#resourcetags): Contains resource tags defined as key/value pairs.
* **type**: 'Microsoft.MachineLearningCompute/operationalizationClusters' (ReadOnly, DeployTimeConstant): The resource type

## Function listKeys (Microsoft.MachineLearningCompute/operationalizationClusters@2017-08-01-preview)
* **Resource**: Microsoft.MachineLearningCompute/operationalizationClusters
* **ApiVersion**: 2017-08-01-preview
* **Output**: [OperationalizationClusterCredentials](#operationalizationclustercredentials)

## OperationalizationClusterProperties
### Properties
* **appInsights**: [AppInsightsProperties](#appinsightsproperties): Properties of App Insights.
* **clusterType**: 'ACS' | 'Local' (Required): The cluster type.
* **containerRegistry**: [ContainerRegistryProperties](#containerregistryproperties): Properties of Azure Container Registry.
* **containerService**: [AcsClusterProperties](#acsclusterproperties): Information about the container service backing the cluster
* **createdOn**: string (ReadOnly): The date and time when the cluster was created.
* **description**: string: The description of the cluster.
* **globalServiceConfiguration**: [GlobalServiceConfiguration](#globalserviceconfiguration): Global configuration for services in the cluster.
* **modifiedOn**: string (ReadOnly): The date and time when the cluster was last modified.
* **provisioningErrors**: [ErrorResponseWrapper](#errorresponsewrapper)[] (ReadOnly): List of provisioning errors reported by the resource provider.
* **provisioningState**: 'Canceled' | 'Creating' | 'Deleting' | 'Failed' | 'Succeeded' | 'Unknown' | 'Updating' (ReadOnly): The provision state of the cluster. Valid values are Unknown, Updating, Provisioning, Succeeded, and Failed.
* **storageAccount**: [StorageAccountProperties](#storageaccountproperties): Properties of Storage Account.

## AppInsightsProperties
### Properties
* **resourceId**: string: ARM resource ID of the App Insights.

## ContainerRegistryProperties
### Properties
* **resourceId**: string: ARM resource ID of the Azure Container Registry used to store Docker images for web services in the cluster. If not provided one will be created. This cannot be changed once the cluster is created.

## AcsClusterProperties
### Properties
* **agentCount**: int: The number of agent nodes in the Container Service. This can be changed to scale the cluster.
* **agentVmSize**: 'Standard_A0' | 'Standard_A1' | 'Standard_A10' | 'Standard_A11' | 'Standard_A2' | 'Standard_A3' | 'Standard_A4' | 'Standard_A5' | 'Standard_A6' | 'Standard_A7' | 'Standard_A8' | 'Standard_A9' | 'Standard_D1' | 'Standard_D11' | 'Standard_D11_v2' | 'Standard_D12' | 'Standard_D12_v2' | 'Standard_D13' | 'Standard_D13_v2' | 'Standard_D14' | 'Standard_D14_v2' | 'Standard_D1_v2' | 'Standard_D2' | 'Standard_D2_v2' | 'Standard_D3' | 'Standard_D3_v2' | 'Standard_D4' | 'Standard_D4_v2' | 'Standard_D5_v2' | 'Standard_DS1' | 'Standard_DS11' | 'Standard_DS12' | 'Standard_DS13' | 'Standard_DS14' | 'Standard_DS2' | 'Standard_DS3' | 'Standard_DS4' | 'Standard_G1' | 'Standard_G2' | 'Standard_G3' | 'Standard_G4' | 'Standard_G5' | 'Standard_GS1' | 'Standard_GS2' | 'Standard_GS3' | 'Standard_GS4' | 'Standard_GS5': The Azure VM size of the agent VM nodes. This cannot be changed once the cluster is created. This list is non exhaustive; refer to https://docs.microsoft.com/en-us/azure/virtual-machines/windows/sizes for the possible VM sizes.
* **clusterFqdn**: string (ReadOnly): The FQDN of the cluster.
* **masterCount**: int: The number of master nodes in the container service.
* **orchestratorProperties**: [KubernetesClusterProperties](#kubernetesclusterproperties): Kubernetes cluster specific properties
* **orchestratorType**: 'Kubernetes' | 'None' (Required): Type of orchestrator. It cannot be changed once the cluster is created.
* **systemServices**: [SystemService](#systemservice)[]: The system services deployed to the cluster

## KubernetesClusterProperties
### Properties
* **servicePrincipal**: [ServicePrincipalProperties](#serviceprincipalproperties): The Azure service principal used by Kubernetes for configuring load balancers

## ServicePrincipalProperties
### Properties
* **clientId**: string (Required): The service principal client ID
* **secret**: string (Required): The service principal secret. This is not returned in response of GET/PUT on the resource. To see this please call listKeys.

## SystemService
### Properties
* **publicIpAddress**: string (ReadOnly): The public IP address of the system service
* **systemServiceType**: 'BatchFrontEnd' | 'None' | 'ScoringFrontEnd' (Required): The system service type
* **version**: string (ReadOnly): The state of the system service

## GlobalServiceConfiguration
### Properties
* **autoScale**: [AutoScaleConfiguration](#autoscaleconfiguration): AutoScale configuration properties.
* **etag**: string: The configuration ETag for updates.
* **serviceAuth**: [ServiceAuthConfiguration](#serviceauthconfiguration): Global service auth configuration properties. These are the data-plane authorization keys and are used if a service doesn't define it's own.
* **ssl**: [SslConfiguration](#sslconfiguration): SSL configuration. If configured data-plane calls to user services will be exposed over SSL only.
### Additional Properties
* **Additional Properties Type**: any

## AutoScaleConfiguration
### Properties
* **maxReplicas**: int: The maximum number of replicas for each service.
* **minReplicas**: int: The minimum number of replicas for each service.
* **refreshPeriodInSeconds**: int: Refresh period in seconds.
* **status**: 'Disabled' | 'Enabled': SSL status. Allowed values are Enabled and Disabled.
* **targetUtilization**: int: The target utilization.

## ServiceAuthConfiguration
### Properties
* **primaryAuthKeyHash**: string (Required): The primary auth key hash. This is not returned in response of GET/PUT on the resource.. To see this please call listKeys API.
* **secondaryAuthKeyHash**: string (Required): The secondary auth key hash. This is not returned in response of GET/PUT on the resource.. To see this please call listKeys API.

## SslConfiguration
### Properties
* **cert**: string: The SSL cert data in PEM format.
* **cname**: string: The CName of the certificate.
* **key**: string: The SSL key data in PEM format. This is not returned in response of GET/PUT on the resource. To see this please call listKeys API.
* **status**: 'Disabled' | 'Enabled': SSL status. Allowed values are Enabled and Disabled.

## ErrorResponseWrapper
### Properties
* **error**: [ErrorResponse](#errorresponse): Error response information.

## ErrorResponse
### Properties
* **code**: string (Required): Error code.
* **details**: [ErrorDetail](#errordetail)[]: An array of error detail objects.
* **message**: string (Required): Error message.

## ErrorDetail
### Properties
* **code**: string (Required): Error code.
* **message**: string (Required): Error message.

## StorageAccountProperties
### Properties
* **resourceId**: string: ARM resource ID of the Azure Storage Account to store CLI specific files. If not provided one will be created. This cannot be changed once the cluster is created.

## ResourceTags
### Properties
### Additional Properties
* **Additional Properties Type**: string

## OperationalizationClusterCredentials
### Properties
* **appInsights**: [AppInsightsCredentials](#appinsightscredentials) (ReadOnly): AppInsights credentials.
* **containerRegistry**: [ContainerRegistryCredentials](#containerregistrycredentials) (ReadOnly): Information about the Azure Container Registry which contains the images deployed to the cluster.
* **containerService**: [ContainerServiceCredentials](#containerservicecredentials) (ReadOnly): Information about the Azure Container Registry which contains the images deployed to the cluster.
* **serviceAuthConfiguration**: [ServiceAuthConfiguration](#serviceauthconfiguration) (ReadOnly): Global service auth configuration properties. These are the data-plane authorization keys and are used if a service doesn't define it's own.
* **sslConfiguration**: [SslConfiguration](#sslconfiguration) (ReadOnly): SSL configuration. If configured data-plane calls to user services will be exposed over SSL only.
* **storageAccount**: [StorageAccountCredentials](#storageaccountcredentials) (ReadOnly): Access information for the storage account.

## AppInsightsCredentials
### Properties
* **appId**: string (ReadOnly): The AppInsights application ID.
* **instrumentationKey**: string (ReadOnly): The AppInsights instrumentation key. This is not returned in response of GET/PUT on the resource. To see this please call listKeys API.

## ContainerRegistryCredentials
### Properties
* **loginServer**: string (ReadOnly): The ACR login server name. User name is the first part of the FQDN.
* **password**: string (ReadOnly): The ACR primary password.
* **password2**: string (ReadOnly): The ACR secondary password.
* **username**: string (ReadOnly): The ACR login username.

## ContainerServiceCredentials
### Properties
* **acsKubeConfig**: string (ReadOnly): The ACS kube config file.
* **imagePullSecretName**: string (ReadOnly): The ACR image pull secret name which was created in Kubernetes.
* **servicePrincipalConfiguration**: [ServicePrincipalProperties](#serviceprincipalproperties) (ReadOnly): The Azure service principal used by Kubernetes for configuring load balancers

## StorageAccountCredentials
### Properties
* **primaryKey**: string (ReadOnly): The primary key of the storage account.
* **resourceId**: string (ReadOnly): The ARM resource ID of the storage account.
* **secondaryKey**: string (ReadOnly): The secondary key of the storage account.

