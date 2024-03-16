---
title: Homebrew
parent: Provider Catalog
---

# Homebrew_Package_Provider

## about_Homebrew_Package_Provider

## Short Description

Provides access to Homebrew.

## Long Description

The Homebrew package provider for `AnyPackage` module lets you use Homebrew using standardized commands.

The Homebrew package provider supports the following cmdlets.

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
provider and are available only when `-Provider Homebrew` parameter is used.

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
