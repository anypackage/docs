---
title: about_Creating_Package_Providers
parent: About
grand_parent: AnyPackage
nav_order: 2
---

# Creating_Package_Providers

## about_Creating_Package_Providers

## Short Description

Describes how to create a package provider.

## Long Description

A package provider is the way for module authors to extend the `AnyPackage`
module. Providers can be created in PowerShell or C#. Package providers are
implemented by defining a class that inherits from `PackageProvider` class and
has the `PackageProvider` attribute.

## Supporting List Available

In order to support `Get-PackageProvider -ListAvailable` the module needs to
define shipped providers. In the module manifest have the following key:

```powershell
@{
    PrivateData = @{
        AnyPackage = @{
            Providers = @('ProviderName')
        }
    }
}
```

## PackageProvider Attribute

The `PackageProvider` attribute defines the package provider name. Additional
configuration may be added in the future to define optional features.

```powershell
[PackageProvider("ProviderName")]
```

### PackageByName

The `PackageByName` optional property can be set to `$false` in order for the
provider to indicate that finding/installing/updating packages by package name
is not supported. This is useful to set if the provider only supports either by
`Path` or `Uri`. The default value is `$true`.

### FileExtensions

The `FileExtensions` optional property is used to indicate which file types are
supported by the package provider when finding/installing/updating packages. To
use the value a string array is used including the proceeding dot. For example
in PowerShell it would be defined like:

`[PackageProvider('Msi', FileExtensions = ('.msi', '.msp')]`

### UriSchemes

The `UriSchemes` optional property is used to indicate which Uri schemes are
supported by the package provider when finding/installing/updating packages. For
example in PowerShell it would be defined like:

`[PackageProvider('MyProvider', UriSchemes = ('http', 'https')]`

## PackageProvider Class

The `PackageProvider` base class serves as the foundation for all package
providers.

### Constructor

The package provider must have a public parameter-less constructor for
`AnyPackage` to call.

### Initializing

`AnyPackage` creates a new instance of the `PackageProvider` each time a cmdlet
is called. This makes the package provider stateless. If a package provider
requires one-time initialization override the `Initialize` method.

If your provider needs to maintain state between instances then you can create a
class that inherits from `PackageProviderInfo` to store state or user accessible
information. The derived `PackageProviderInfo` will be sent to each instance of
the package provider.

```powershell
[PackageProvider('Test')]
class TestProvider : PackageProvider {
    [PackageProviderInfo] Initialize([PackageProviderInfo] $providerInfo) {
        return [MyProviderInfo]::new()
    }
}

class MyProviderInfo : PackageProviderInfo {
    [SqlConnection] $Connection
}
```

### Uninitializing

To perform one-time provider clean-up to free up any resources or connections
override the `Clean` method.

```powershell
[PackageProvider('Test')]
class TestProvider : PackageProvider {
    [void] Clean() {
        # Clean-up logic 
    }
}
```

## Supported Sources

If the package provider supports finding/updating/installing/saving packages
with a source override the `IsSource([string] $source)` method. The default
implementation is to always return `$true`.

In this example, the method defines `production` and `testing` as supported
sources. When an `AnyPackage` cmdlet is called it will call the `IsSource`
method and validate the provider supports the source.

```powershell
[bool] IsSource([string] $source) {
    return $source -in 'production', 'testing'
}
```

### Dynamic Parameters

To add provider specific parameters for a command override the
`GetDynamicParameters` method. The `$commandName` parameter will be one of the
cmdlets such as `Get-Package`. The method can return `$null`, a
`[RuntimeDefinedParameterDictionary]` object or an object with properties that
have `[Parameter()]` attribute.

Defining a class with properties is the easiest way to create dynamic
parameters. The syntax is very similar to the `param()` block in a PowerShell
function. There are few notable differences, one being that each property must
have a `[Parameter()]` attribute in order for the PowerShell runtime to treat it
as a parameter. Secondly there is no comma after each parameter.

```powershell
[PackageProvider('Test')]
class TestProvider : PackageProvider {
    [object] GetDynamicParameters([string] $commandName) {
        if ($commandName -eq 'Get-Package') {
            return [GetPackageDynamicParameters]::new()
        } else {
            return $null
        }
    }
}

class GetPackageDynamicParameters {
    [Parameter()]
    [string] $Path

    [Parameter()]
    [ScopeType] $Scope
}
```

### Supporting Operations

The package provider indicates support for each individual `AnyPackage` cmdlet
by adding a corresponding interface. For example, if the package provider
supports `Get-Package` cmdlet then the `IGetPackage` interface would be
implemented.

| Cmdlet                       | Interface         |
| ------                       | ---------         |
| Find-Package                 | IFindPackage      |
| Get-Package                  | IGetPackage       |
| Install-Package              | IInstallPackage   |
| Publish-Package              | IPublishPackage   |
| Save-Package                 | ISavePackage      |
| Update-Package               | IUpdatePackage    |
| Uninstall-Package            | IUninstallPackage |
| Get-PackageSource            | IGetSource        |
| Set-PackageSource            | ISetSource        |
| Register-PackageSource       | ISetSource        |
| Unregister-PackageSource     | ISetSource        |

If a `Package` method was successful `WritePackage` must be called with the
package details. In the event a package is not found by the provider do not
throw an exception as `AnyPackage` will write an error.

The package interfaces follow the structure as follows.

```powershell
[PackageProvider('Test')]
class TestProvider : PackageProvider, IGetPackage {
    [void] GetPackage([PackageRequest] $request) { }
}
```

If a `Source` method was successful `WriteSource` must be called with the source
details. In the event a source is not found by the provider do not throw an
exception as `AnyPackage` will write an error.

The package source interfaces follow the structure as follows.

```powershell
[PackageProvider('Test')]
class TestProvider : PackageProvider, IGetSource {
    [void] GetPackageSource([SourceRequest] $request) { }
}
```

The `ISetSource` interface is different as it requires three methods compared to
the rest.

```powershell
[PackageProvider('Test')]
class TestProvider : PackageProvider, ISetSource {
    [void] SetPackageSource([SourceRequest] $request) { }

    [void] RegisterPackageSource([SourceRequest] $request) { }

    [void] UnregisterPackageSource([SourceRequest] $request) { }
}
```

### Package Request

The `[PackageRequest]` type contains information about the request and methods
to interact with `AnyPackage`.

```powershell
class PackageRequest {
    [string] $Name
    [PackageVersionRange] $Version
    [string] $Source
    [bool] $Prerelease
    [PackageInfo] $Package
    [string] $Path
    [Uri] $Uri
    [object] $DynamicParameters
    [PackageProviderInfo] $ProviderInfo

    [bool] $Stopping

    [bool] IsMatch([string] $name)
    [bool] IsMatch([PackageVersion] $version)
    [bool] IsMatch([string] $name, [PackageVersion] $version)

    [bool] PromptUntrustedSource([string] $source)

    [void] WritePackage([PackageInfo] $package)
```

### Source Request

The `[SourceRequest]` type contains information about the request and methods to
interact with `AnyPackage`.

```powershell
class SourceRequest {
    [string] $Name
    [string] $Location
    [bool] $Trusted
    [bool] $Force
    [object] $DynamicParameters
    [PackageProviderInfo] $ProviderInfo

    [bool] $Stopping

    [void] WriteSource([PackageSourceInfo] $source)
```

## Register a Package Provider

To register a package provider with `AnyPackage` the following method must be
called from within your module. In this example the `[TestProvider]` is the type
that implements the package provider and `e5491948-72b3-4f00-aa64-f93060d9b242`
is the provider's unique ID..

```powershell
[guid] $id = 'e5491948-72b3-4f00-aa64-f93060d9b242'
[PackageProviderManager]::RegisterProvider($id, [TestProvider], $MyInvocation.MyCommand.ScriptBlock.Module)
```

If you are unable to pass the `PSModuleInfo` then the module name can be passed
instead.

```powershell
[guid] $id = 'e5491948-72b3-4f00-aa64-f93060d9b242'
[PackageProviderManager]::RegisterProvider($id, [TestProvider], 'TestModule')
```

## Unregister a Package Provider

To remove a package provider on when the provider module is removed set the
`OnRemove` property for the module calling the
`[PackageProviderManager]::UnregisterProvider([Guid] $id)` method.

In the example the following example, the `e5491948-72b3-4f00-aa64-f93060d9b242`
is the provider's unique ID.

```powershell
$MyInvocation.MyCommand.ScriptBlock.Module.OnRemove = { 
    [PackageProviderManager]::UnregisterProvider('e5491948-72b3-4f00-aa64-f93060d9b242')
}
```

## Packages without a Version

If your package provider supports packages without a version special
consideration needs to take place. The user may specify all versions to be
returned and in that case packages with a `null` version should also be
returned.

In this example the `$request.IsMatch($name)` method is used to filter package
names. Then an additional check is used if the `$request.Version` is `null` or
is a `*` all version wildcard.

```powershell
if ($request.IsMatch($name) -and ($null -eq $request.Version -or $request.Version -eq '*') {
    # Write package
}
```

## Examples

### Basic Provider

The following example is the minimum code required to define a package provider.

```powershell
using module AnyPackage
using namespace AnyPackage.Provider

[PackageProvider('Test')]
class TestProvider : PackageProvider { }

[guid] $id = 'e5491948-72b3-4f00-aa64-f93060d9b242'
[PackageProviderManager]::RegisterProvider($id, [TestProvider], $MyInvocation.MyCommand.ScriptBlock.Module)

$MyInvocation.MyCommand.ScriptBlock.Module.OnRemove = { 
    [PackageProviderManager]::UnregisterProvider($id)
}
```

## Documenting

The package provider should come with an about topic to describe the provider
any capabilities it has and any dynamic parameters.

## See Also

- [about_Package_Providers](about_Package_Providers.md)
- [about_AnyPackage](about_AnyPackage.md)
