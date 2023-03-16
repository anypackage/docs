---
external help file: AnyPackage.dll-Help.xml
Module Name: AnyPackage
online version: https://go.anypackage.dev/Get-Package
parent: AnyPackage
schema: 2.0.0
---

# Get-Package

## SYNOPSIS

Gets installed packages.

## SYNTAX

```
Get-Package [[-Name] <String[]>] [[-Version] <PackageVersionRange>] [-Provider <String>] [<CommonParameters>]
```

## DESCRIPTION

Gets installed packages.

## EXAMPLES

### Example 1: Gets all packages

```powershell
PS C:\> Get-Package

Name                                     Version         Source               Provider
----                                     -------         ----------           --------
Microsoft.PowerShell.Archive             1.2.5.0         PSGallery            PowerShellGet
Microsoft.PowerShell.ConsoleGuiTools     0.7.2.0         PSGallery            PowerShellGet
```

The command gets packages from registered package providers.

### Example 2: Gets all package from a provider

```powershell
PS C:\> Get-Package -Provider PowerShellGet

Name                                     Version         Source               Provider
----                                     -------         ----------           --------
Microsoft.PowerShell.Archive             1.2.5.0         PSGallery            PowerShellGet
Microsoft.PowerShell.ConsoleGuiTools     0.7.2.0         PSGallery            PowerShellGet
```

The command gets packages from `PowerShellGet` package provider.

## PARAMETERS

### -Name

Specifies the package name.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: *
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: True
```

### -Provider

Specifies the package provider.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Version

Specifies the package version.
The format is NuGet version range syntax with minor changes.
In normal NuGet version range value of `1.0` would be minimum version inclusive but this parameter converts that value to be exact version of `[1.0]`.
If you need to have minimum version inclusive then use this format `[1.0,]`.
For more information refer to [NuGet version range syntax](https://learn.microsoft.com/en-us/nuget/concepts/package-versioning#version-ranges).

```yaml
Type: PackageVersionRange
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### System.String, AnyPackage.Provider.PackageVersionRange

You can pipe a package name and version range to this cmdlet.

## OUTPUTS

### AnyPackage.Provider.PackageInfo

This cmdlet returns objects that represent a package.

## NOTES

## RELATED LINKS

[Find-Package](Find-Package.md)

[Install-Package](Install-Package.md)

[Publish-Package](Publish-Package.md)

[Save-Package](Save-Package.md)

[Update-Package](Update-Package.md)

[Uninstall-Package](Uninstall-Package.md)
