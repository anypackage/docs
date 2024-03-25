---
title: .NET Tool
parent: Provider Catalog
---

# DotNet-Tool_Package_Provider

## about_DotNet-Tool_Package_Provider

## Short Description

Provides access to .NET Tool package manager.

## Long Description

The Windows .NET Tool package provider for `AnyPackage` module lets you get .NET Tools from nuget.org

The .NET Tool package provider supports the following cmdlets.

* Find-Package
* Get-Package
* Install-Package
* Update-Package
* Uninstall-Package

## Dynamic Parameters

Dynamic parameters are cmdlet parameters that are added by a package
provider and are available only when `-Provider '.NET Tool'` parameter is used.

The .NET Tool provider currently has no dynamic parameters.

## See Also

* [about_Package_Providers](../../reference/about_Package_Providers.md)
* [about_AnyPackage](../../reference/about_AnyPackage.md)
