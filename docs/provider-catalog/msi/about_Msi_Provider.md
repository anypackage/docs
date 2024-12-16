---
title: Msi
parent: Provider Catalog
---

# Msi_Package_Provider

## about_Msi_Package_Provider

## Short Description

Provides access to Windows programs.

## Long Description

The Windows programs package provider for `AnyPackage` module lets you manage
Windows Installer.

The Msi package provider supports the following cmdlets.

- Find-Package
- Get-Package
- Install-Package
- Uninstall-Package

## Dynamic Parameters

Dynamic parameters are cmdlet parameters that are added by a package provider
and are available only when `-Provider Msi` parameter is used.

### InstallType \<AnyPackage.Provider.Msi.InstallType\>

Specifies the type of Windows installer to return. Default value is `All`.

Valid values are:

- Product
- Patch
- All

#### Cmdlets Supported

- Get-Package

### Properties \<System.String[]\>

Specifies the MSI properties to install.

#### Cmdlets Supported

- Install-Package

## See Also

- [about_Package_Providers](../../reference/about_Package_Providers.md)
- [about_AnyPackage](../../reference/about_AnyPackage.md)
