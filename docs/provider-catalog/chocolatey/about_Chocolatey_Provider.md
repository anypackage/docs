---
title: Chocolatey
parent: Provider Catalog
---

# Chocolatey_Package_Provider

## about_Chocolatey_Package_Provider

## Short Description

Provides access to Chocolatey.

## Long Description

The Chocolatey package provider for `AnyPackage` module lets you use Chocolatey using standardized commands.

The Chocolatey package provider supports the following cmdlets.

* Find-Package
* Get-Package
* Get-PackageSource
* Install-Package
* Register-PackageSource
* Set-PackageSource
* Uninstall-Package
* Unregister-PackageSource

## Dynamic Parameters

Dynamic parameters are cmdlet parameters that are added by a package
provider and are available only when `-Provider Chocolatey` parameter is used.

### Params <System.String>

Parameters to pass to the package being installed.

#### Cmdlets Supported

* Install-Package

### ParamsGlobal <System.Management.Automation.SwitchParameter>

Apply package parameters to dependencies of package being installed.

#### Cmdlets Supported

* Install-Package

### RemoveDependencies <System.Management.Automation.SwitchParameter>

Uninstall dependencies of package being uninstalled.

#### Cmdlets Supported

* Uninstall-Package

## See Also

* [about_Package_Providers](../../reference/about_Package_Providers.md)
* [about_AnyPackage](../../reference/about_AnyPackage.md)
