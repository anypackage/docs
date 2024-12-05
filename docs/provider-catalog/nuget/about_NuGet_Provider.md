---
title: NuGet
parent: Provider Catalog
---

# NuGet_Package_Provider

## about_NuGet_Package_Provider

## Short Description

Provides access to NuGet packages.

## Long Description

The NuGet provider for `AnyPackage` module lets you manage NuGet packages.

The NuGet package provider supports the following cmdlets.

- Find-Package
- Get-Package
- Get-PackageSource
- Install-Package
- Register-PackageSource
- Save-Package
- Set-PackageSource
- Uninstall-Package
- Unregister-PackageSource

## Dynamic Parameters

Dynamic parameters are cmdlet parameters that are added by a package provider
and are available only when `-Provider NuGet` parameter is used.

### DependencyBehavior \<System.String\>

Specifies the dependency resolution behavior when resolving versions. For more
information refer to [dependency resolution] page.

Behaviors supported are:

- Lowest
- HighestPatch
- HighestMinor
- Highest

#### Cmdlets Supported

- Install-Package
- Save-Package

### Framework \<System.String\>

Specifies the target framework for use in dependency resolution. For a list of
available frameworks use the [Target Frameworks][framework] page and use the TFM
name.

#### Cmdlets Supported

- Install-Package
- Save-Package

## See Also

- [about_Package_Providers](../../reference/about_Package_Providers.md)
- [about_AnyPackage](../../reference/about_AnyPackage.md)

[framework]: https://learn.microsoft.com/en-us/nuget/reference/target-frameworks
[dependency resolution]: https://learn.microsoft.com/en-us/nuget/concepts/dependency-resolution