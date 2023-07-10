---
title: DSC
has_children: true
nav_order: 4
has_toc: false
---

# Desired State Configuration

## Installing AnyPackageDsc

To install AnyPackage use the built-in PowerShell package manager.

Launch PowerShell and run the following command.

```powershell
# PowerShellGet
Install-Module AnyPackageDsc

# PSResourceGet
Install-PSResource AnyPackageDsc
```

## Resources

### [Package](Package.md)

Configures a package.

### [Source](Source.md)

Configures a package source.
