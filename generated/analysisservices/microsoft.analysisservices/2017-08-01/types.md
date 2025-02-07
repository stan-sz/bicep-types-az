# Microsoft.AnalysisServices @ 2017-08-01

## Resource Microsoft.AnalysisServices/servers@2017-08-01
* **Valid Scope(s)**: ResourceGroup
### Properties
* **apiVersion**: '2017-08-01' (ReadOnly, DeployTimeConstant): The resource api version
* **id**: string (ReadOnly, DeployTimeConstant): The resource id
* **location**: string (Required): Location of the Analysis Services resource.
* **name**: string (Required, DeployTimeConstant): The resource name
* **properties**: [AnalysisServicesServerProperties](#analysisservicesserverproperties): Properties of Analysis Services resource.
* **sku**: [ResourceSku](#resourcesku) (Required): Represents the SKU name and Azure pricing tier for Analysis Services resource.
* **tags**: [ResourceTags](#resourcetags): Key-value pairs of additional resource provisioning properties.
* **type**: 'Microsoft.AnalysisServices/servers' (ReadOnly, DeployTimeConstant): The resource type

## Function listGatewayStatus (Microsoft.AnalysisServices/servers@2017-08-01)
* **Resource**: Microsoft.AnalysisServices/servers
* **ApiVersion**: 2017-08-01
* **Output**: [GatewayListStatusLive](#gatewayliststatuslive)

## AnalysisServicesServerProperties
### Properties
* **asAdministrators**: [ServerAdministrators](#serveradministrators): An array of administrator user identities.
* **backupBlobContainerUri**: string: The SAS container URI to the backup container.
* **gatewayDetails**: [GatewayDetails](#gatewaydetails): The gateway details.
* **ipV4FirewallSettings**: [IPv4FirewallSettings](#ipv4firewallsettings): An array of firewall rules.
* **managedMode**: int: The managed mode of the server (0 = not managed, 1 = managed).
* **provisioningState**: 'Deleting' | 'Failed' | 'Paused' | 'Pausing' | 'Preparing' | 'Provisioning' | 'Resuming' | 'Scaling' | 'Succeeded' | 'Suspended' | 'Suspending' | 'Updating' (ReadOnly): The current deployment state of Analysis Services resource. The provisioningState is to indicate states for resource provisioning.
* **querypoolConnectionMode**: 'All' | 'ReadOnly': How the read-write server's participation in the query pool is controlled.<br/>It can have the following values: <ul><li>readOnly - indicates that the read-write server is intended not to participate in query operations</li><li>all - indicates that the read-write server can participate in query operations</li></ul>Specifying readOnly when capacity is 1 results in error.
* **serverFullName**: string (ReadOnly): The full name of the Analysis Services resource.
* **serverMonitorMode**: int: The server monitor mode for AS server
* **sku**: [ResourceSku](#resourcesku): Represents the SKU name and Azure pricing tier for Analysis Services resource.
* **state**: 'Deleting' | 'Failed' | 'Paused' | 'Pausing' | 'Preparing' | 'Provisioning' | 'Resuming' | 'Scaling' | 'Succeeded' | 'Suspended' | 'Suspending' | 'Updating' (ReadOnly): The current state of Analysis Services resource. The state is to indicate more states outside of resource provisioning.

## ServerAdministrators
### Properties
* **members**: string[]: An array of administrator user identities.

## GatewayDetails
### Properties
* **dmtsClusterUri**: string (ReadOnly): Uri of the DMTS cluster.
* **gatewayObjectId**: string (ReadOnly): Gateway object id from in the DMTS cluster for the gateway resource.
* **gatewayResourceId**: string: Gateway resource to be associated with the server.

## IPv4FirewallSettings
### Properties
* **enablePowerBIService**: bool: The indicator of enabling PBI service.
* **firewallRules**: [IPv4FirewallRule](#ipv4firewallrule)[]: An array of firewall rules.

## IPv4FirewallRule
### Properties
* **firewallRuleName**: string: The rule name.
* **rangeEnd**: string: The end range of IPv4.
* **rangeStart**: string: The start range of IPv4.

## ResourceSku
### Properties
* **capacity**: int: The number of instances in the read only query pool.
* **name**: string (Required): Name of the SKU level.
* **tier**: 'Basic' | 'Development' | 'Standard': The name of the Azure pricing tier to which the SKU applies.

## ResourceTags
### Properties
### Additional Properties
* **Additional Properties Type**: string

## GatewayListStatusLive
### Properties
* **status**: '0' (ReadOnly): Live message of list gateway. Status: 0 - Live

