---
title: PowerShellGet
parent: Provider Catalog
---

# PowerShellGet_Package_Provider

## about_PowerShellGet_Package_Provider

## Short Description

Provides access to PowerShellGet.

## Long Description

The PowerShellGet package provider for `AnyPackage` module lets you use PowerShellGet using standardized commands.

The PowerShellGet package provider supports the following cmdlets.

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
provider and are available only when `-Provider PowerShellGet` parameter is used.

### Path <System.String>

Specifies the search path.

#### Cmdlets Supported

* Get-Package

### Scope \<Microsoft.PowerShell.PowerShellGet.UtilClasses.ScopeType\>

Specifies the scope of the resource.

#### Cmdlets Supported

* Get-Package

### Scope \<Microsoft.PowerShell.PowerShellGet.UtilClasses.ScopeType\>

Specifies the scope of the resource. Scope types supported are:

* CurrentUser
* AllUsers

#### Cmdlets Supported

* Get-Package

### Tag \<System.String\>

Filters search results for resources that include one or more of the specified tags.

#### Cmdlets Supported

* Find-Package

### Type \<Microsoft.PowerShell.PowerShellGet.UtilClasses.ResourceType\>

Specifies one or more resource types to find. Resource types supported are:

* Module
* Script
* Command
* DscResource

#### Cmdlets Supported

* Find-Package

## See Also

* [about_Package_Providers](../../reference/about_Package_Providers.md)
* [about_AnyPackage](../../reference/about_AnyPackage.md)
