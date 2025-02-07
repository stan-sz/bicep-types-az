# Microsoft.CertificateRegistration @ 2021-03-01

## Resource Microsoft.CertificateRegistration/certificateOrders@2021-03-01
* **Valid Scope(s)**: ResourceGroup
### Properties
* **apiVersion**: '2021-03-01' (ReadOnly, DeployTimeConstant): The resource api version
* **id**: string (ReadOnly, DeployTimeConstant): The resource id
* **kind**: string: Kind of resource.
* **location**: string (Required): Resource Location.
* **name**: string (Required, DeployTimeConstant): The resource name
* **properties**: [AppServiceCertificateOrderProperties](#appservicecertificateorderproperties): AppServiceCertificateOrder resource specific properties
* **tags**: [ResourceTags](#resourcetags): Resource tags.
* **type**: 'Microsoft.CertificateRegistration/certificateOrders' (ReadOnly, DeployTimeConstant): The resource type

## Resource Microsoft.CertificateRegistration/certificateOrders/certificates@2021-03-01
* **Valid Scope(s)**: ResourceGroup
### Properties
* **apiVersion**: '2021-03-01' (ReadOnly, DeployTimeConstant): The resource api version
* **id**: string (ReadOnly, DeployTimeConstant): The resource id
* **kind**: string: Kind of resource.
* **location**: string (Required): Resource Location.
* **name**: string (Required, DeployTimeConstant): The resource name
* **properties**: [AppServiceCertificate](#appservicecertificate): Key Vault container for a certificate that is purchased through Azure.
* **tags**: [ResourceTags](#resourcetags): Resource tags.
* **type**: 'Microsoft.CertificateRegistration/certificateOrders/certificates' (ReadOnly, DeployTimeConstant): The resource type

## AppServiceCertificateOrderProperties
### Properties
* **appServiceCertificateNotRenewableReasons**: 'ExpirationNotInRenewalTimeRange' | 'RegistrationStatusNotSupportedForRenewal' | 'SubscriptionNotActive'[] (ReadOnly): Reasons why App Service Certificate is not renewable at the current moment.
* **autoRenew**: bool: <code>true</code> if the certificate should be automatically renewed when it expires; otherwise, <code>false</code>.
* **certificates**: [AppServiceCertificateOrderPropertiesCertificates](#appservicecertificateorderpropertiescertificates): State of the Key Vault secret.
* **contact**: [CertificateOrderContact](#certificateordercontact) (ReadOnly)
* **csr**: string: Last CSR that was created for this order.
* **distinguishedName**: string: Certificate distinguished name.
* **domainVerificationToken**: string (ReadOnly): Domain verification token.
* **expirationTime**: string (ReadOnly): Certificate expiration time.
* **intermediate**: [CertificateDetails](#certificatedetails) (ReadOnly): SSL certificate details.
* **isPrivateKeyExternal**: bool (ReadOnly): <code>true</code> if private key is external; otherwise, <code>false</code>.
* **keySize**: int: Certificate key size.
* **lastCertificateIssuanceTime**: string (ReadOnly): Certificate last issuance time.
* **nextAutoRenewalTimeStamp**: string (ReadOnly): Time stamp when the certificate would be auto renewed next
* **productType**: 'StandardDomainValidatedSsl' | 'StandardDomainValidatedWildCardSsl' (Required): Certificate product type.
* **provisioningState**: 'Canceled' | 'Deleting' | 'Failed' | 'InProgress' | 'Succeeded' (ReadOnly): Status of certificate order.
* **root**: [CertificateDetails](#certificatedetails) (ReadOnly): SSL certificate details.
* **serialNumber**: string (ReadOnly): Current serial number of the certificate.
* **signedCertificate**: [CertificateDetails](#certificatedetails) (ReadOnly): SSL certificate details.
* **status**: 'Canceled' | 'Denied' | 'Expired' | 'Issued' | 'NotSubmitted' | 'PendingRekey' | 'Pendingissuance' | 'Pendingrevocation' | 'Revoked' | 'Unused' (ReadOnly): Current order status.
* **validityInYears**: int: Duration in years (must be 1).

## AppServiceCertificateOrderPropertiesCertificates
### Properties
### Additional Properties
* **Additional Properties Type**: [AppServiceCertificate](#appservicecertificate)

## AppServiceCertificate
### Properties
* **keyVaultId**: string: Key Vault resource Id.
* **keyVaultSecretName**: string: Key Vault secret name.
* **provisioningState**: 'AzureServiceUnauthorizedToAccessKeyVault' | 'CertificateOrderFailed' | 'ExternalPrivateKey' | 'Initialized' | 'KeyVaultDoesNotExist' | 'KeyVaultSecretDoesNotExist' | 'OperationNotPermittedOnKeyVault' | 'Succeeded' | 'Unknown' | 'UnknownError' | 'WaitingOnCertificateOrder' (ReadOnly): Status of the Key Vault secret.

## CertificateOrderContact
### Properties
* **email**: string
* **nameFirst**: string
* **nameLast**: string
* **phone**: string

## CertificateDetails
### Properties
* **issuer**: string (ReadOnly): Certificate Issuer.
* **notAfter**: string (ReadOnly): Date Certificate is valid to.
* **notBefore**: string (ReadOnly): Date Certificate is valid from.
* **rawData**: string (ReadOnly): Raw certificate data.
* **serialNumber**: string (ReadOnly): Certificate Serial Number.
* **signatureAlgorithm**: string (ReadOnly): Certificate Signature algorithm.
* **subject**: string (ReadOnly): Certificate Subject.
* **thumbprint**: string (ReadOnly): Certificate Thumbprint.
* **version**: int (ReadOnly): Certificate Version.

## ResourceTags
### Properties
### Additional Properties
* **Additional Properties Type**: string

## ResourceTags
### Properties
### Additional Properties
* **Additional Properties Type**: string

