# Microsoft.Capacity @ 2021-07-01

## Resource Microsoft.Capacity/reservationOrders@2021-07-01
* **Valid Scope(s)**: Tenant
### Properties
* **apiVersion**: '2021-07-01' (ReadOnly, DeployTimeConstant): The resource api version
* **etag**: int (ReadOnly)
* **id**: string (ReadOnly, DeployTimeConstant): The resource id
* **location**: string (WriteOnly): The Azure Region where the reserved resource lives.
* **name**: string (Required, DeployTimeConstant): The resource name
* **properties**: [PurchaseRequestProperties](#purchaserequestproperties)
* **sku**: [SkuName](#skuname) (WriteOnly)
* **systemData**: [SystemData](#systemdata) (ReadOnly): Metadata pertaining to creation and last modification of the resource.
* **type**: 'Microsoft.Capacity/reservationOrders' (ReadOnly, DeployTimeConstant): The resource type

## PurchaseRequestProperties
### Properties
* **appliedScopes**: string[] (WriteOnly): List of the subscriptions that the benefit will be applied. Do not specify if AppliedScopeType is Shared.
* **appliedScopeType**: 'Shared' | 'Single' (WriteOnly): Type of the Applied Scope.
* **billingPlan**: 'Monthly' | 'Upfront': Represent the billing plans.
* **billingScopeId**: string (WriteOnly): Subscription that will be charged for purchasing Reservation
* **createdDateTime**: string (ReadOnly): This is the DateTime when the reservation was created.
* **displayName**: string: Friendly name of the Reservation
* **expiryDate**: string (ReadOnly): This is the date when the Reservation will expire.
* **originalQuantity**: int (ReadOnly): Total Quantity of the SKUs purchased in the Reservation.
* **planInformation**: [ReservationOrderBillingPlanInformation](#reservationorderbillingplaninformation) (ReadOnly): Information describing the type of billing plan for this reservation.
* **provisioningState**: 'BillingFailed' | 'Cancelled' | 'ConfirmedBilling' | 'ConfirmedResourceHold' | 'Created' | 'Creating' | 'Expired' | 'Failed' | 'Merged' | 'PendingBilling' | 'PendingResourceHold' | 'Split' | 'Succeeded' (ReadOnly): Represent the current state of the Reservation.
* **quantity**: int (WriteOnly): Quantity of the SKUs that are part of the Reservation. Must be greater than zero.
* **renew**: bool (WriteOnly): Setting this to true will automatically purchase a new reservation on the expiration date time.
* **requestDateTime**: string (ReadOnly): This is the DateTime when the reservation was initially requested for purchase.
* **reservations**: [ReservationResponse](#reservationresponse)[] (ReadOnly): Array of ReservationResponse
* **reservedResourceProperties**: [PurchaseRequestPropertiesReservedResourceProperties](#purchaserequestpropertiesreservedresourceproperties) (WriteOnly): Properties specific to each reserved resource type. Not required if not applicable.
* **reservedResourceType**: 'AVS' | 'AppService' | 'AzureDataExplorer' | 'AzureFiles' | 'BlockBlob' | 'CosmosDb' | 'DataFactory' | 'Databricks' | 'DedicatedHost' | 'ManagedDisk' | 'MariaDb' | 'MySql' | 'NetAppStorage' | 'PostgreSql' | 'RedHat' | 'RedHatOsa' | 'RedisCache' | 'SapHana' | 'SqlAzureHybridBenefit' | 'SqlDataWarehouse' | 'SqlDatabases' | 'SqlEdge' | 'SuseLinux' | 'VMwareCloudSimple' | 'VirtualMachines' (WriteOnly): The type of the resource that is being reserved.
* **term**: 'P1Y' | 'P3Y' | 'P5Y': Represent the term of Reservation.

## ReservationOrderBillingPlanInformation
### Properties
* **nextPaymentDueDate**: string (ReadOnly): For recurring billing plans, indicates the date when next payment will be processed. Null when total is paid off.
* **pricingCurrencyTotal**: [Price](#price) (ReadOnly)
* **startDate**: string (ReadOnly): Date when the billing plan has started.
* **transactions**: [PaymentDetail](#paymentdetail)[] (ReadOnly): Array of PaymentDetail

## Price
### Properties
* **amount**: int (ReadOnly)
* **currencyCode**: string (ReadOnly): The ISO 4217 3-letter currency code for the currency used by this purchase record.

## PaymentDetail
### Properties
* **billingAccount**: string (ReadOnly): Shows the Account that is charged for this payment.
* **billingCurrencyTotal**: [Price](#price) (ReadOnly)
* **dueDate**: string (ReadOnly): Date when the payment needs to be done.
* **extendedStatusInfo**: [ExtendedStatusInfo](#extendedstatusinfo) (ReadOnly)
* **paymentDate**: string (ReadOnly): Date when the transaction is completed. Is null when it is scheduled.
* **pricingCurrencyTotal**: [Price](#price) (ReadOnly)
* **status**: 'Cancelled' | 'Failed' | 'Scheduled' | 'Succeeded' (ReadOnly): Describes whether the payment is completed, failed, cancelled or scheduled in the future.

## ExtendedStatusInfo
### Properties
* **message**: string (ReadOnly): The message giving detailed information about the status code.
* **statusCode**: 'Active' | 'Expired' | 'Merged' | 'None' | 'PaymentInstrumentError' | 'Pending' | 'PurchaseError' | 'Split' | 'Succeeded' (ReadOnly)

## ReservationResponse
### Properties
* **etag**: int (ReadOnly)
* **id**: string (ReadOnly): Identifier of the reservation
* **kind**: 'Microsoft.Compute' (ReadOnly): Resource Provider type to be reserved.
* **location**: string (ReadOnly): The Azure Region where the reserved resource lives.
* **name**: string (ReadOnly): Name of the reservation
* **properties**: [ReservationsProperties](#reservationsproperties) (ReadOnly): The properties of the reservations
* **sku**: [SkuName](#skuname) (ReadOnly)
* **systemData**: [SystemData](#systemdata) (ReadOnly): Metadata pertaining to creation and last modification of the resource.
* **type**: string (ReadOnly): Type of resource. "Microsoft.Capacity/reservationOrders/reservations"

## ReservationsProperties
### Properties
* **appliedScopes**: string[] (ReadOnly): List of the subscriptions that the benefit will be applied. Do not specify if AppliedScopeType is Shared.
* **appliedScopeType**: 'Shared' | 'Single' (ReadOnly): Type of the Applied Scope.
* **archived**: bool (ReadOnly): Indicates if the reservation is archived
* **billingPlan**: 'Monthly' | 'Upfront' (ReadOnly): Represent the billing plans.
* **billingScopeId**: string (ReadOnly): Subscription that will be charged for purchasing Reservation
* **capabilities**: string (ReadOnly): Capabilities of the reservation
* **displayName**: string (ReadOnly): Friendly name for user to easily identify the reservation
* **displayProvisioningState**: string (ReadOnly): The provisioning state of the reservation for display, e.g. Succeeded
* **effectiveDateTime**: string (ReadOnly): DateTime of the Reservation starting when this version is effective from.
* **expiryDate**: string (ReadOnly): This is the date when the Reservation will expire.
* **extendedStatusInfo**: [ExtendedStatusInfo](#extendedstatusinfo) (ReadOnly)
* **instanceFlexibility**: 'Off' | 'On' (ReadOnly): Turning this on will apply the reservation discount to other VMs in the same VM size group. Only specify for VirtualMachines reserved resource type.
* **lastUpdatedDateTime**: string (ReadOnly): DateTime of the last time the Reservation was updated.
* **mergeProperties**: [ReservationMergeProperties](#reservationmergeproperties) (ReadOnly)
* **provisioningState**: 'BillingFailed' | 'Cancelled' | 'ConfirmedBilling' | 'ConfirmedResourceHold' | 'Created' | 'Creating' | 'Expired' | 'Failed' | 'Merged' | 'PendingBilling' | 'PendingResourceHold' | 'Split' | 'Succeeded' (ReadOnly): Represent the current state of the Reservation.
* **provisioningSubState**: string (ReadOnly): The provisioning state of the reservation, e.g. Succeeded
* **purchaseDate**: string (ReadOnly): This is the date when the Reservation was purchased.
* **quantity**: int (ReadOnly): Quantity of the SKUs that are part of the Reservation. Must be greater than zero.
* **renew**: bool (ReadOnly): Setting this to true will automatically purchase a new reservation on the expiration date time.
* **renewDestination**: string (ReadOnly): Reservation Id of the reservation which is purchased because of renew. Format of the resource Id is /providers/Microsoft.Capacity/reservationOrders/{reservationOrderId}/reservations/{reservationId}.
* **renewProperties**: [RenewPropertiesResponse](#renewpropertiesresponse) (ReadOnly)
* **renewSource**: string (ReadOnly): Reservation Id of the reservation from which this reservation is renewed. Format of the resource Id is /providers/Microsoft.Capacity/reservationOrders/{reservationOrderId}/reservations/{reservationId}.
* **reservedResourceType**: 'AVS' | 'AppService' | 'AzureDataExplorer' | 'AzureFiles' | 'BlockBlob' | 'CosmosDb' | 'DataFactory' | 'Databricks' | 'DedicatedHost' | 'ManagedDisk' | 'MariaDb' | 'MySql' | 'NetAppStorage' | 'PostgreSql' | 'RedHat' | 'RedHatOsa' | 'RedisCache' | 'SapHana' | 'SqlAzureHybridBenefit' | 'SqlDataWarehouse' | 'SqlDatabases' | 'SqlEdge' | 'SuseLinux' | 'VMwareCloudSimple' | 'VirtualMachines' (ReadOnly): The type of the resource that is being reserved.
* **skuDescription**: string (ReadOnly): Description of the SKU in english.
* **splitProperties**: [ReservationSplitProperties](#reservationsplitproperties) (ReadOnly)
* **term**: 'P1Y' | 'P3Y' | 'P5Y' (ReadOnly): Represent the term of Reservation.
* **userFriendlyAppliedScopeType**: string (ReadOnly): The applied scope type of the reservation for display, e.g. Shared
* **userFriendlyRenewState**: string (ReadOnly): The renew state of the reservation for display, e.g. On
* **utilization**: [ReservationsPropertiesUtilization](#reservationspropertiesutilization) (ReadOnly): Reservation utilization

## ReservationMergeProperties
### Properties
* **mergeDestination**: string (ReadOnly): Reservation Resource Id Created due to the merge. Format of the resource Id is /providers/Microsoft.Capacity/reservationOrders/{reservationOrderId}/reservations/{reservationId}
* **mergeSources**: string[] (ReadOnly): Resource Ids of the Source Reservation's merged to form this Reservation. Format of the resource Id is /providers/Microsoft.Capacity/reservationOrders/{reservationOrderId}/reservations/{reservationId}

## RenewPropertiesResponse
### Properties
* **billingCurrencyTotal**: [RenewPropertiesResponseBillingCurrencyTotal](#renewpropertiesresponsebillingcurrencytotal) (ReadOnly): Currency and amount that customer will be charged in customer's local currency for renewal purchase. Tax is not included.
* **pricingCurrencyTotal**: [RenewPropertiesResponsePricingCurrencyTotal](#renewpropertiesresponsepricingcurrencytotal) (ReadOnly): Amount that Microsoft uses for record. Used during refund for calculating refund limit. Tax is not included. This is locked price 30 days before expiry.
* **purchaseProperties**: [PurchaseRequest](#purchaserequest) (ReadOnly)

## RenewPropertiesResponseBillingCurrencyTotal
### Properties
* **amount**: int (ReadOnly)
* **currencyCode**: string (ReadOnly): The ISO 4217 3-letter currency code for the currency used by this purchase record.

## RenewPropertiesResponsePricingCurrencyTotal
### Properties
* **amount**: int (ReadOnly)
* **currencyCode**: string (ReadOnly): The ISO 4217 3-letter currency code for the currency used by this purchase record.

## PurchaseRequest
### Properties
* **location**: string (ReadOnly): The Azure Region where the reserved resource lives.
* **properties**: [PurchaseRequestProperties](#purchaserequestproperties) (ReadOnly)
* **sku**: [SkuName](#skuname) (ReadOnly)

## SkuName
### Properties
* **name**: string (WriteOnly)

## ReservationSplitProperties
### Properties
* **splitDestinations**: string[] (ReadOnly): List of destination Resource Id that are created due to split. Format of the resource Id is /providers/Microsoft.Capacity/reservationOrders/{reservationOrderId}/reservations/{reservationId}
* **splitSource**: string (ReadOnly): Resource Id of the Reservation from which this is split. Format of the resource Id is /providers/Microsoft.Capacity/reservationOrders/{reservationOrderId}/reservations/{reservationId}

## ReservationsPropertiesUtilization
### Properties
* **aggregates**: [ReservationUtilizationAggregates](#reservationutilizationaggregates)[] (ReadOnly): The array of aggregates of a reservation's utilization
* **trend**: string (ReadOnly): The number of days trend for a reservation

## ReservationUtilizationAggregates
### Properties
* **grain**: int (ReadOnly): The grain of the aggregate
* **grainUnit**: string (ReadOnly): The grain unit of the aggregate
* **value**: int (ReadOnly): The aggregate value
* **valueUnit**: string (ReadOnly): The aggregate value unit

## SystemData
### Properties
* **createdAt**: string (ReadOnly): The timestamp of resource creation (UTC).
* **createdBy**: string (ReadOnly): The identity that created the resource.
* **createdByType**: 'Application' | 'Key' | 'ManagedIdentity' | 'User' (ReadOnly): The type of identity that created the resource.
* **lastModifiedAt**: string (ReadOnly): The timestamp of resource last modification (UTC)
* **lastModifiedBy**: string (ReadOnly): The identity that last modified the resource.
* **lastModifiedByType**: 'Application' | 'Key' | 'ManagedIdentity' | 'User' (ReadOnly): The type of identity that created the resource.

## PurchaseRequestPropertiesReservedResourceProperties
### Properties
* **instanceFlexibility**: 'Off' | 'On' (WriteOnly): Turning this on will apply the reservation discount to other VMs in the same VM size group. Only specify for VirtualMachines reserved resource type.

