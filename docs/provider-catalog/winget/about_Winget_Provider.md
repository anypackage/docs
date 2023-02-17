---
title: Winget
parent: Provider Catalog
---

# Winget_Package_Provider

## about_Winget_Package_Provider

## Short Description

Provides access to Winget.

## Long Description

The Winget package provider for `AnyPackage` module lets you use Winget using standardized commands.

The Winget package provider supports the following cmdlets.

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
provider and are available only when `-Provider Winget` parameter is used.

The Winget provider currently has no dynamic parameters. 

## See Also

* [about_Package_Providers](../../reference/about_Package_Providers.md)
* [about_AnyPackage](../../reference/about_AnyPackage.md)
