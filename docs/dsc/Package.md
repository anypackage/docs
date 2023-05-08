---
parent: DSC
---

# Package

The `Package` DSC resource is used to configure AnyPackage packages.

## Syntax

```text
Package [String] #ResourceName
{
    Name = [string]
    Provider = [string]
    Version = [string]
    [AdditionalParameters = [HashTable]]
    [Ensure = [string]{ Absent | Present }]
    [Latest = [bool]]
    [Prerelease = [bool]]
    [Source = [string]]
}
```

## Properties

### AdditionalParameters

Specifies provider dynamic parameters.

```yaml
Attribute: Write
Type: HashTable
Default value: None
```

### Ensure

Specifies if the package should be installed.

```yaml
Attribute: Write
Type: bool
Default value: Present
```

### Latest

Specifies if the latest package should be installed.

```yaml
Attribute: Write
Type: bool
Default value: False
```

### Name

Specifies the package name.

```yaml
Attribute: Key
Type: string
Default value: None
```

### Prerelease

Specifies if prerelease packages should installed.

```yaml
Attribute: Write
Type: bool
Default value: False
```

### Provider

Specifies the package provider full name.
The provider full name is in the following format: ModuleName\ProviderName.
For AnyPackage PowerShellGet provider it would be: AnyPackage.PowerShellGet\PowerShellGet.

```yaml
Attribute: Key
Type: string
Default value: None
```

### Reasons

Returns reasons why the resource is not in compliance.
The `Code` property is the unique identifier and `Phrase` property is the human readable reason.

```yaml
Attribute: Read
Type: string
Default value: N/A
```

### Source

Specifies the package source.

```yaml
Attribute: Required
Type: string
Default value: None
```

### Version

Specifies the package version.
The format is NuGet version range syntax with minor changes.
To specify any package version use `*`.
In normal NuGet version range value of `1.0` would be minimum version inclusive but this parameter converts that value to be exact version of `[1.0]`.
If you need to have minimum version inclusive then use this format `[1.0,]`.
For more information refer to [NuGet version range syntax](https://learn.microsoft.com/en-us/nuget/concepts/package-versioning#version-ranges).

```yaml
Attribute: Key
Type: string
Default value: None
```
