---
title: PSResourceGet
parent: Provider Catalog
---

# PSResourceGet_Package_Provider

## about_PSResourceGet_Package_Provider

## Short Description

Provides access to PSResourceGet.

## Long Description

The PSResourceGet package provider for `AnyPackage` module lets you use PSResourceGet using standardized commands.

The PSResourceGet package provider supports the following cmdlets.

* Find-Package
* Get-Package
* Get-PackageSource
* Install-Package
* Publish-Package
* Register-PackageSource
* Save-Package
* Set-PackageSource
* Uninstall-Package
* Unregister-PackageSource
* Update-Package

## Dynamic Parameters

Dynamic parameters are cmdlet parameters that are added by a package
provider and are available only when `-Provider PSResourceGet` parameter is used.

### ApiKey \<System.String\>

Specifies the API key that you want to use to publish a resource to the online gallery.

#### Cmdlets Supported

* Publish-Package

### AcceptLicense \<System.Management.Automation.SwitchParameter\>

Specifies that the resource should accept any request to accept the license agreement.
This suppresses prompting if the module mandates that a user accept the license agreement.

#### Cmdlets Supported

* Install-Package
* Update-Package

### AuthenticodeCheck \<System.Management.Automation.SwitchParameter\>

Validates Authenticode signatures and catalog files on Windows.

#### Cmdlets Supported

* Install-Package
* Save-Package
* Update-Package

### Credential \<System.Management.Automation.PSCredential\>

Optional credentials to be used when accessing a repository.

#### Cmdlets Supported

* Find-Package
* Install-Package
* Publish-Package
* Save-Package
* Update-Package

### CredentialInfo \<Microsoft.PowerShell.PSResourceGet.UtilClasses.PSCredentialInfo\>

A PSCredentialInfo object that includes the name of a vault and a secret that is stored in a Microsoft.PowerShell.SecretManagement store.

#### Cmdlets Supported

* Register-PackageSource
* Set-PackageSource

### DestinationPath \<System.String\>

Specifies the path where the NuGet package `.nupkg` file should be saved.
This parameter can be used in conjunction with the Source parameter to publish to a source and also save the exact same package to the local file system.

#### Cmdlets Supported

* Publish-Package

### Force \<System.Management.Automation.SwitchParameter\>

When specified, bypasses checks for TrustRepository and AcceptLicense and updates the package.

#### Cmdlets Supported

* Update-Package

### IncludeDependencies \<System.Management.Automation.SwitchParameter\>

When specified, search returns all matching resources their dependencies.
Dependencies are deduplicated.

#### Cmdlets Supported

* Find-Package

### Latest \<System.Management.Automation.SwitchParameter\>

Returns the latest package for a given version range.

#### Cmdlets Supported

* Find-Package

### Path \<System.String\>

Specifies the search path.

#### Cmdlets Supported

* Get-Package

### Priority \<System.Int32\>

Specifies the priority ranking of the repository.
Valid priority values range from 0 to 100.
Lower values have a higher priority ranking. The default value is `100`.

Repositories are searched in priority order (highest first).

#### Cmdlets Supported

* Register-PackageSource
* Set-PackageSource

### Proxy \<System.Uri\>

The URL to a proxy server used to access repositories outside of your network.

#### Cmdlets Supported

* Publish-Package

### ProxyCredential \<System.Management.Automation.PSCredential\>

The credentials required to use the proxy server.

#### Cmdlets Supported

* Publish-Package

### PSGallery \<System.Management.Automation.SwitchParameter\>

When specified, registers PSGallery repository.

#### Cmdlets Supported

* Register-PackageSource

### Reinstall \<System.Management.Automation.SwitchParameter\>

Installs the latest version of a module even if the latest version is already installed.
The installed version is overwritten.
This allows you to repair a damaged installation of the module.

If an older version of the module is installed, the new version is installed side-by-side in a new version-specific folder.

#### Cmdlets Supported

* Install-Package

### Scope \<Microsoft.PowerShell.PSResourceGet.UtilClasses.ScopeType\>

Specifies the scope of the resource.
Scope types supported are:

* CurrentUser
* AllUsers

#### Cmdlets Supported

* Get-Package
* Install-Package
* Uninstall-Package
* Update-Package

### SkipDependenciesCheck \<System.Management.Automation.SwitchParameter\>

Bypasses the default check that all dependencies are present in the target repository.

#### Cmdlets Supported

* Publish-Package

### SkipDependencyCheck \<System.Management.Automation.SwitchParameter\>

Skips the check for resource dependencies. Only found resources are installed.
No resources of the found resource are installed.

#### Cmdlets Supported

* Install-Package
* Save-Package
* Uninstall-Package
* Update-Package

### SkipModuleManifestValidate \<System.Management.Automation.SwitchParameter\>

Skips validating the module manifest before publishing.

#### Cmdlets Supported

* Publish-Package

### Tag \<System.String\>

Filters search results for resources that include one or more of the specified tags.

#### Cmdlets Supported

* Find-Package

### TemporaryPath \<System.String\>

Specifies the path to temporarily install the resource before actual installation.
If no temporary path is provided, the resource is temporarily installed in the current user's temporary folder.

#### Cmdlets Supported

* Install-Package
* Save-Package
* Update-Package

### Type \<Microsoft.PowerShell.PSResourceGet.UtilClasses.ResourceType\>

Specifies one or more resource types to find.
Resource types supported are:

* Module
* Script
* Command
* DscResource

#### Cmdlets Supported

* Find-Package

## See Also

* [about_Package_Providers](../../reference/about_Package_Providers.md)
* [about_AnyPackage](../../reference/about_AnyPackage.md)
