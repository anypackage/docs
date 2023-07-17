---
title: Programs
parent: Provider Catalog
---

# Programs_Package_Provider

## about_Programs_Package_Provider

## Short Description

Provides access to Windows programs.

## Long Description

The Windows programs package provider for `AnyPackage` module lets you get Windows Add/Remove programs using standardized commands.

The Programs package provider supports the following cmdlets.

* Get-Package
* Uninstall-Package

## Dynamic Parameters

Dynamic parameters are cmdlet parameters that are added by a package
provider and are available only when `-Provider Programs` parameter is used.

### SystemComponent \<System.Management.Automation.SwitchParameter\>

Includes Windows system components.

#### Cmdlets Supported

* Get-Package

## See Also

* [about_Package_Providers](../../reference/about_Package_Providers.md)
* [about_AnyPackage](../../reference/about_AnyPackage.md)
