---
title: Scoop
parent: Provider Catalog
---

# Scoop_Package_Provider

## about_Scoop_Package_Provider

## Short Description

Provides access to Scoop.

## Long Description

The Scoop package provider for `AnyPackage` module lets you use Scoop using
standardized commands.

The Scoop package provider supports the following cmdlets.

- Find-Package
- Get-Package
- Get-PackageSource
- Install-Package
- Optimize-Package
- Register-PackageSource
- Set-PackageSource
- Uninstall-Package
- Unregister-PackageSource
- Update-Package

## Dynamic Parameters

Dynamic parameters are cmdlet parameters that are added by a package provider
and are available only when `-Provider Scoop` parameter is used.

### Architecture \<System.String\>

Specifies the app architecture.
Scope types supported are:

- 32bit
- 64bit
- arm64

#### Cmdlets Supported

- Install-Package
- Uninstall-Package
- Update-Package

### DownloadCache \<System.Management.Automation.SwitchParameter\>

Remove outdated download cache.

#### Cmdlets Supported

- Optimize-Package

### NoCache \<System.Management.Automation.SwitchParameter\>

Does not use the download cache.

#### Cmdlets Supported

- Install-Package
- Update-Package

### Official \<System.String\>

Specifies an official bucket.

#### Cmdlets Supported

- Register-PackageSource

### Reinstall \<System.Management.Automation.SwitchParameter\>

Reinstalls the app even if there is not a newer version.

#### Cmdlets Supported

- Update-Package

### RemoveData \<System.String\>

Remove all persistent data.

#### Cmdlets Supported

- Uninstall-Package

### Scope \<System.String\>

Specifies the scope of the package.
Scope types supported are:

- CurrentUser
- AllUsers

#### Cmdlets Supported

- Install-Package
- Uninstall-Package
- Update-Package

### SkipDependencies \<System.Management.Automation.SwitchParameter\>

Skip installing app dependencies.

#### Cmdlets Supported

- Install-Package
- Update-Package

### SkipHashCheck \<System.Management.Automation.SwitchParameter\>

Skips hash validation.

#### Cmdlets Supported

- Install-Package
- Update-Package

## See Also

- [about_Package_Providers](../../reference/about_Package_Providers.md)
- [about_AnyPackage](../../reference/about_AnyPackage.md)
