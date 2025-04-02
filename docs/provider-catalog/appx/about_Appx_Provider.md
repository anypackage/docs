---
title: Appx
parent: Provider Catalog
---

# Appx_Package_Provider

## about_Appx_Package_Provider

## Short Description

Provides access to Appx.

## Long Description

The Appx package provider for `AnyPackage` module lets you use Appx using
standardized commands.

The Appx package provider supports the following cmdlets.

- Find-Package
- Get-Package
- Install-Package
- Uninstall-Package

## Dynamic Parameters

Dynamic parameters are cmdlet parameters that are added by a package provider
and are available only when `-Provider Appx` parameter is used.

### AllUsers \<System.Management.Automation.SwitchParameter\>

Indicates that this cmdlet lists app packages for all user accounts on the
computer. To use this parameter, you must run the command with administrator
permissions.

#### Cmdlets Supported

- Get-Package

### PackageTypeFilter \<Windows.Management.Deployment.PackageTypes\>

Specifies one or more comma-separated types of packages that the cmdlet gets
from the package repository.

By default, this cmdlet returns only packages of types Main and Framework.

PackageTypeFilter types supported are:

- Main
- Framework
- Resource
- Bundle
- Xap
- Optional

#### Cmdlets Supported

- Get-Package

### Publisher \<System.String\>

Specifies the publisher of a particular package. If you specify this parameter,
the cmdlet returns results only for this publisher. Wildcards are permitted.

#### Cmdlets Supported

- Get-Package

### Volume \<Microsoft.Windows.Appx.PackageManager.Commands.AppxVolume\>

Specifies an AppxVolume object. If you specify this parameter, this cmdlet
returns only packages that are relative to volume that this parameter specifies.

#### Cmdlets Supported

- Get-Package

### User \<System.String\>

Specifies a user. If you specify this parameter, the cmdlet returns a list of
app packages that are installed for only the user that this cmdlet specifies. To
get the list of packages for a user profile other than the profile for the
current user, you must run this command with administrator permissions. The user
name can be in one of these formats:

- domain\user_name
- user_name\@fqn.domain.tld
- user_name
- SID-string

#### Cmdlets Supported

- Get-Package
- Uninstall-Package

### PreserveRoamableApplicationData \<System.Management.Automation.SwitchParameter\>

Preserves the roamable portion of the app's data when the package is removed.
This parameter is incompatible with PreserveApplicationData.

#### Cmdlets Supported

- Uninstall-Package

### PreserveApplicationData \<System.Management.Automation.SwitchParameter\>

Specifies that the cmdlet preserves the application data during the package
removal. The application data is available for later use. Note that this is only
applicable for apps that are under development so this option can only be
specified for apps that are registered from file layout (Loose file registered).

#### Cmdlets Supported

- Uninstall-Package

## See Also

- [about_Package_Providers](../../reference/about_Package_Providers.md)
- [about_AnyPackage](../../reference/about_AnyPackage.md)
