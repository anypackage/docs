---
title: ModuleFast
parent: Provider Catalog
---

# ModuleFast_Package_Provider

## about_ModuleFast_Package_Provider

## Short Description

Provides access to PowerShell module ModuleFast.

## Long Description

The ModuleFast package provider for `AnyPackage` module lets you interact with
ModuleFast using standardized commands.

The Programs package provider supports the following cmdlets.

- Find-Package
- Install-Package

## Dynamic Parameters

Dynamic parameters are cmdlet parameters that are added by a package provider
and are available only when `-Provider ModuleFast` parameter is used.

### Destination \<System.String\>

Where to install the modules. This defaults to the builtin module path on
non-windows and a custom LOCALAPPDATA location on Windows. You can also specify
'CurrentUser' to install to the Documents folder on Windows Only (this is not
recommended)

#### Cmdlets Supported

- Install-Package

### ThrottleLimit \<System.Int32\>

How many concurrent installation threads to run. Each installation thread, given
sufficient bandwidth, will likely saturate a full CPU core with decompression
work. This defaults to the number of logical cores on the system. If your system
uses HyperThreading and presents more logical cores than physical cores
available, you may want to set this to half your number of logical cores for
best performance.

#### Cmdlets Supported

- Install-Package

### CILockFilePath \<System.String\>

The path to the lockfile. By default it is requires.lock.json in the current
folder. This is ignored if -CI parameter is not present. It is generally not
recommended to change this setting.

#### Cmdlets Supported

- Install-Package

### Update \<System.Management.Automation.SwitchParameter\>

Setting this will check for newer modules if your installed modules are not
already at the upper bound of the required version range. Note that specifying
this will also clear the local request cache for remote repositories which will
result in slower evaluations if the information has not changed.

#### Cmdlets Supported

- Install-Package

### NoProfileUpdate \<System.Management.Automation.SwitchParameter\>

Setting this won't add the default destination to your `powershell.config.json`.
This really only matters on Windows.

#### Cmdlets Supported

- Install-Package

### NoPSModulePathUpdate \<System.Management.Automation.SwitchParameter\>

By default will modify your PSModulePath to use the builtin destination if not
present. Setting this implicitly skips profile update as well.

#### Cmdlets Supported

- Install-Package

## See Also

- [about_Package_Providers](../../reference/about_Package_Providers.md)
- [about_AnyPackage](../../reference/about_AnyPackage.md)
