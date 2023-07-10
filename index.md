---
nav_order: 1
---

# Home

## What is AnyPackage?

AnyPackage is not a package management system in the traditional sense but rather a way to interact with multiple package management systems.
This lets users have a single set of commands to interact with any package management system.

AnyPackage is built on PowerShell giving users the ability to manage Windows, Linux, and Mac.

## What is a Package Provider?

A package provider is the interface for AnyPackage to interact with the various package management systems.
See the [provider catalog](/docs/provider-catalog/provider-catalog.md) for the list of package providers.

## Installing AnyPackage

To install AnyPackage use the built-in PowerShell package manager.

Launch PowerShell and run the following command.

```powershell
# PowerShellGet
Install-Module AnyPackage

# PSResourceGet
Install-PSResource AnyPackage
```
