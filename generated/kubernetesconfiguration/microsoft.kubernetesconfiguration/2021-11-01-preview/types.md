# Microsoft.KubernetesConfiguration @ 2021-11-01-preview

## Resource Microsoft.KubernetesConfiguration/extensions@2021-11-01-preview
* **Valid Scope(s)**: Extension
### Properties
* **apiVersion**: '2021-11-01-preview' (ReadOnly, DeployTimeConstant): The resource api version
* **id**: string (ReadOnly, DeployTimeConstant): The resource id
* **identity**: [Identity](#identity): Identity for the resource.
* **name**: string (Required, DeployTimeConstant): The resource name
* **properties**: [ExtensionProperties](#extensionproperties): Properties of an Extension resource
* **systemData**: [SystemData](#systemdata) (ReadOnly): Metadata pertaining to creation and last modification of the resource.
* **type**: 'Microsoft.KubernetesConfiguration/extensions' (ReadOnly, DeployTimeConstant): The resource type

## Resource Microsoft.KubernetesConfiguration/fluxConfigurations@2021-11-01-preview
* **Valid Scope(s)**: Extension
### Properties
* **apiVersion**: '2021-11-01-preview' (ReadOnly, DeployTimeConstant): The resource api version
* **id**: string (ReadOnly, DeployTimeConstant): The resource id
* **name**: string (Required, DeployTimeConstant): The resource name
* **properties**: [FluxConfigurationProperties](#fluxconfigurationproperties): Properties to create a Flux Configuration resource
* **systemData**: [SystemData](#systemdata) (ReadOnly): Metadata pertaining to creation and last modification of the resource.
* **type**: 'Microsoft.KubernetesConfiguration/fluxConfigurations' (ReadOnly, DeployTimeConstant): The resource type

## Resource Microsoft.KubernetesConfiguration/sourceControlConfigurations@2021-11-01-preview
* **Valid Scope(s)**: Extension
### Properties
* **apiVersion**: '2021-11-01-preview' (ReadOnly, DeployTimeConstant): The resource api version
* **id**: string (ReadOnly, DeployTimeConstant): The resource id
* **name**: string (Required, DeployTimeConstant): The resource name
* **properties**: [SourceControlConfigurationProperties](#sourcecontrolconfigurationproperties): Properties to create a Source Control Configuration resource
* **systemData**: [SystemData](#systemdata) (ReadOnly): Metadata pertaining to creation and last modification of the resource.
* **type**: 'Microsoft.KubernetesConfiguration/sourceControlConfigurations' (ReadOnly, DeployTimeConstant): The resource type

## Identity
### Properties
* **principalId**: string (ReadOnly): The principal ID of resource identity.
* **tenantId**: string (ReadOnly): The tenant ID of resource.
* **type**: 'SystemAssigned': The identity type.

## ExtensionProperties
### Properties
* **aksAssignedIdentity**: [ExtensionPropertiesAksAssignedIdentity](#extensionpropertiesaksassignedidentity): Identity of the Extension resource in an AKS cluster
* **autoUpgradeMinorVersion**: bool: Flag to note if this extension participates in auto upgrade of minor version, or not.
* **configurationProtectedSettings**: [ExtensionPropertiesConfigurationProtectedSettings](#extensionpropertiesconfigurationprotectedsettings): Configuration settings that are sensitive, as name-value pairs for configuring this extension.
* **configurationSettings**: [ExtensionPropertiesConfigurationSettings](#extensionpropertiesconfigurationsettings): Configuration settings, as name-value pairs for configuring this extension.
* **customLocationSettings**: [ExtensionPropertiesCustomLocationSettings](#extensionpropertiescustomlocationsettings) (ReadOnly): Custom Location settings properties.
* **errorInfo**: [ErrorDetail](#errordetail) (ReadOnly): The error detail.
* **extensionType**: string: Type of the Extension, of which this resource is an instance of.  It must be one of the Extension Types registered with Microsoft.KubernetesConfiguration by the Extension publisher.
* **packageUri**: string (ReadOnly): Uri of the Helm package
* **provisioningState**: 'Canceled' | 'Creating' | 'Deleting' | 'Failed' | 'Succeeded' | 'Updating' (ReadOnly): The provisioning state of the resource.
* **releaseTrain**: string: ReleaseTrain this extension participates in for auto-upgrade (e.g. Stable, Preview, etc.) - only if autoUpgradeMinorVersion is 'true'.
* **scope**: [Scope](#scope): Scope of the extension. It can be either Cluster or Namespace; but not both.
* **statuses**: [ExtensionStatus](#extensionstatus)[]: Status from this extension.
* **version**: string: Version of the extension for this extension, if it is 'pinned' to a specific version. autoUpgradeMinorVersion must be 'false'.

## ExtensionPropertiesAksAssignedIdentity
### Properties
* **principalId**: string (ReadOnly): The principal ID of resource identity.
* **tenantId**: string (ReadOnly): The tenant ID of resource.
* **type**: 'SystemAssigned': The identity type.

## ExtensionPropertiesConfigurationProtectedSettings
### Properties
### Additional Properties
* **Additional Properties Type**: string

## ExtensionPropertiesConfigurationSettings
### Properties
### Additional Properties
* **Additional Properties Type**: string

## ExtensionPropertiesCustomLocationSettings
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

## Scope
### Properties
* **cluster**: [ScopeCluster](#scopecluster): Specifies that the scope of the extension is Cluster
* **namespace**: [ScopeNamespace](#scopenamespace): Specifies that the scope of the extension is Namespace

## ScopeCluster
### Properties
* **releaseNamespace**: string: Namespace where the extension Release must be placed, for a Cluster scoped extension.  If this namespace does not exist, it will be created

## ScopeNamespace
### Properties
* **targetNamespace**: string: Namespace where the extension will be created for an Namespace scoped extension.  If this namespace does not exist, it will be created

## ExtensionStatus
### Properties
* **code**: string: Status code provided by the Extension
* **displayStatus**: string: Short description of status of the extension.
* **level**: 'Error' | 'Information' | 'Warning': Level of the status.
* **message**: string: Detailed message of the status from the Extension.
* **time**: string: DateLiteral (per ISO8601) noting the time of installation status.

## SystemData
### Properties
* **createdAt**: string: The timestamp of resource creation (UTC).
* **createdBy**: string: The identity that created the resource.
* **createdByType**: 'Application' | 'Key' | 'ManagedIdentity' | 'User': The type of identity that created the resource.
* **lastModifiedAt**: string: The timestamp of resource last modification (UTC)
* **lastModifiedBy**: string: The identity that last modified the resource.
* **lastModifiedByType**: 'Application' | 'Key' | 'ManagedIdentity' | 'User': The type of identity that created the resource.

## FluxConfigurationProperties
### Properties
* **complianceState**: 'Compliant' | 'Non-Compliant' | 'Pending' | 'Suspended' | 'Unknown' (ReadOnly): Compliance state of the cluster object.
* **configurationProtectedSettings**: [FluxConfigurationPropertiesConfigurationProtectedSettings](#fluxconfigurationpropertiesconfigurationprotectedsettings): Key-value pairs of protected configuration settings for the configuration
* **errorMessage**: string (ReadOnly): Error message returned to the user in the case of provisioning failure.
* **gitRepository**: [GitRepositoryDefinition](#gitrepositorydefinition): Parameters to reconcile to the GitRepository source kind type.
* **kustomizations**: [FluxConfigurationPropertiesKustomizations](#fluxconfigurationpropertieskustomizations): Array of kustomizations used to reconcile the artifact pulled by the source type on the cluster.
* **lastSourceSyncedAt**: string (ReadOnly): Datetime the fluxConfiguration last synced its source on the cluster.
* **lastSourceSyncedCommitId**: string (ReadOnly): Branch and SHA of the last source commit synced with the cluster.
* **namespace**: string: The namespace to which this configuration is installed to. Maximum of 253 lower case alphanumeric characters, hyphen and period only.
* **provisioningState**: 'Canceled' | 'Creating' | 'Deleting' | 'Failed' | 'Succeeded' | 'Updating' (ReadOnly): The provisioning state of the resource.
* **repositoryPublicKey**: string (ReadOnly): Public Key associated with this fluxConfiguration (either generated within the cluster or provided by the user).
* **scope**: 'cluster' | 'namespace': Scope at which the configuration will be installed.
* **sourceKind**: 'GitRepository': Source Kind to pull the configuration data from.
* **statuses**: [ObjectStatusDefinition](#objectstatusdefinition)[] (ReadOnly): Statuses of the Flux Kubernetes resources created by the fluxConfiguration or created by the managed objects provisioned by the fluxConfiguration.
* **suspend**: bool: Whether this configuration should suspend its reconciliation of its kustomizations and sources.

## FluxConfigurationPropertiesConfigurationProtectedSettings
### Properties
### Additional Properties
* **Additional Properties Type**: string

## GitRepositoryDefinition
### Properties
* **httpsCAFile**: string: Base64-encoded HTTPS certificate authority contents used to access git private git repositories over HTTPS
* **httpsUser**: string: Base64-encoded HTTPS username used to access private git repositories over HTTPS
* **localAuthRef**: string: Name of a local secret on the Kubernetes cluster to use as the authentication secret rather than the managed or user-provided configuration secrets.
* **repositoryRef**: [RepositoryRefDefinition](#repositoryrefdefinition): The source reference for the GitRepository object.
* **sshKnownHosts**: string: Base64-encoded known_hosts value containing public SSH keys required to access private git repositories over SSH
* **syncIntervalInSeconds**: int: The interval at which to re-reconcile the cluster git repository source with the remote.
* **timeoutInSeconds**: int: The maximum time to attempt to reconcile the cluster git repository source with the remote.
* **url**: string: The URL to sync for the flux configuration git repository.

## RepositoryRefDefinition
### Properties
* **branch**: string: The git repository branch name to checkout.
* **commit**: string: The commit SHA to checkout. This value must be combined with the branch name to be valid. This takes precedence over semver.
* **semver**: string: The semver range used to match against git repository tags. This takes precedence over tag.
* **tag**: string: The git repository tag name to checkout. This takes precedence over branch.

## FluxConfigurationPropertiesKustomizations
### Properties
### Additional Properties
* **Additional Properties Type**: [KustomizationDefinition](#kustomizationdefinition)

## KustomizationDefinition
### Properties
* **dependsOn**: [DependsOnDefinition](#dependsondefinition)[]: Specifies other Kustomizations that this Kustomization depends on. This Kustomization will not reconcile until all dependencies have completed their reconciliation.
* **force**: bool: Enable/disable re-creating Kubernetes resources on the cluster when patching fails due to an immutable field change.
* **path**: string: The path in the source reference to reconcile on the cluster.
* **prune**: bool: Enable/disable garbage collections of Kubernetes objects created by this Kustomization.
* **retryIntervalInSeconds**: int: The interval at which to re-reconcile the Kustomization on the cluster in the event of failure on reconciliation.
* **syncIntervalInSeconds**: int: The interval at which to re-reconcile the Kustomization on the cluster.
* **timeoutInSeconds**: int: The maximum time to attempt to reconcile the Kustomization on the cluster.
* **validation**: 'client' | 'none' | 'server': Specify whether to validate the Kubernetes objects referenced in the Kustomization before applying them to the cluster.

## DependsOnDefinition
### Properties
* **kustomizationName**: string: Name of the kustomization to claim dependency on

## ObjectStatusDefinition
### Properties
* **appliedBy**: [ObjectReferenceDefinition](#objectreferencedefinition): Object reference to a Kubernetes object on a cluster
* **complianceState**: 'Compliant' | 'Non-Compliant' | 'Pending' | 'Suspended' | 'Unknown': Compliance state of the cluster object.
* **helmReleaseProperties**: [HelmReleasePropertiesDefinition](#helmreleasepropertiesdefinition)
* **kind**: string: Kind of the applied object
* **name**: string: Name of the applied object
* **namespace**: string: Namespace of the applied object
* **statusConditions**: [ObjectStatusConditionDefinition](#objectstatusconditiondefinition)[]: List of Kubernetes object status conditions present on the cluster

## ObjectReferenceDefinition
### Properties
* **name**: string: Name of the object
* **namespace**: string: Namespace of the object

## HelmReleasePropertiesDefinition
### Properties
* **failureCount**: int: Total number of times that the HelmRelease failed to install or upgrade
* **helmChartRef**: [ObjectReferenceDefinition](#objectreferencedefinition): Object reference to a Kubernetes object on a cluster
* **installFailureCount**: int: Number of times that the HelmRelease failed to install
* **lastRevisionApplied**: int: The revision number of the last released object change
* **upgradeFailureCount**: int: Number of times that the HelmRelease failed to upgrade

## ObjectStatusConditionDefinition
### Properties
* **lastTransitionTime**: string: Last time this status condition has changed
* **message**: string: A more verbose description of the object status condition
* **reason**: string: Reason for the specified status condition type status
* **status**: string: Status of the Kubernetes object condition type
* **type**: string: Object status condition type for this object

## SourceControlConfigurationProperties
### Properties
* **complianceStatus**: [ComplianceStatus](#compliancestatus) (ReadOnly): Compliance Status details
* **configurationProtectedSettings**: [ConfigurationProtectedSettings](#configurationprotectedsettings): Name-value pairs of protected configuration settings for the configuration
* **enableHelmOperator**: bool: Option to enable Helm Operator for this git configuration.
* **helmOperatorProperties**: [HelmOperatorProperties](#helmoperatorproperties): Properties for Helm operator.
* **operatorInstanceName**: string: Instance name of the operator - identifying the specific configuration.
* **operatorNamespace**: string: The namespace to which this operator is installed to. Maximum of 253 lower case alphanumeric characters, hyphen and period only.
* **operatorParams**: string: Any Parameters for the Operator instance in string format.
* **operatorScope**: 'cluster' | 'namespace': Scope at which the operator will be installed.
* **operatorType**: 'Flux': Type of the operator
* **provisioningState**: 'Accepted' | 'Deleting' | 'Failed' | 'Running' | 'Succeeded' (ReadOnly): The provisioning state of the resource provider.
* **repositoryPublicKey**: string (ReadOnly): Public Key associated with this SourceControl configuration (either generated within the cluster or provided by the user).
* **repositoryUrl**: string: Url of the SourceControl Repository.
* **sshKnownHostsContents**: string: Base64-encoded known_hosts contents containing public SSH keys required to access private Git instances

## ComplianceStatus
### Properties
* **complianceState**: 'Compliant' | 'Failed' | 'Installed' | 'Noncompliant' | 'Pending' (ReadOnly): The compliance state of the configuration.
* **lastConfigApplied**: string: Datetime the configuration was last applied.
* **message**: string: Message from when the configuration was applied.
* **messageLevel**: 'Error' | 'Information' | 'Warning': Level of the message.

## ConfigurationProtectedSettings
### Properties
### Additional Properties
* **Additional Properties Type**: string

## HelmOperatorProperties
### Properties
* **chartValues**: string: Values override for the operator Helm chart.
* **chartVersion**: string: Version of the operator Helm chart.

