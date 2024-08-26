---
nav_order: 5
permalink: docs/security
---

# Security

AnyPackage is an extensible package management interface. Logic in the package
provider is usually limited to structuring calls to the package manager. This
presents some security considerations as package provider, package manager, and
packages must be trusted by the user.

## Definitions

- AnyPackage - PowerShell module and API for user interaction with package
  providers.
- Package Provider - An implementation of the AnyPackage API shipped in a
  PowerShell module.
- Package Manager - The package lifecycle logic for example: WinGet, Chocolatey,
  Scoop, APT, DNF, etc.

## Package Providers

Only import trusted package providers.

AnyPackage project package providers are signed. Third party created package
providers may not be signed. PowerShell [execution policies] provide controls to
prohibit unsigned modules from being imported.

[execution policies]: https://learn.microsoft.com/en-us/powershell/module/microsoft.powershell.core/about/about_execution_policies

## Packages

Only install packages from trusted sources.

AnyPackage itself does not perform any validation checks on packages returned by
the package provider. AnyPackage relies on the package manager to perform those
checks. Refer to each package manager documentation for policies on package
validation. An example is the [Chocolatey community repository].

[Chocolatey community repository]: https://docs.chocolatey.org/en-us/information/security/#security-for-the-community-package-repository
