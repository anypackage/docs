---
external help file: AnyPackage.dll-Help.xml
Module Name: AnyPackage
online version: https://go.anypackage.dev/Find-Package
parent: AnyPackage
schema: 2.0.0
---

# Find-Package

## SYNOPSIS

Finds packages in package sources.

## SYNTAX

### Name

```
Find-Package [[-Name] <String[]>] [[-Version] <PackageVersionRange>] [-Source <String>] [-Prerelease]
 [-Provider <String>] [<CommonParameters>]
```

### Path

```
Find-Package -Path <String[]> [-Provider <String>] [<CommonParameters>]
```

### LiteralPath

```
Find-Package -LiteralPath <String[]> [-Provider <String>]
 [<CommonParameters>]
```

### Uri

```
Find-Package -Uri <Uri[]> [-Provider <String>] [<CommonParameters>]
```

## DESCRIPTION

Finds packages in package sources.

## EXAMPLES

### Example 1: Find all packages

```powershell
PS C:\> Find-Package

Name                                     Version         Source               Provider
----                                     -------         ----------           --------
Microsoft.PowerShell.Archive             1.2.5.0         PSGallery            PowerShellGet
Microsoft.PowerShell.ConsoleGuiTools     0.7.2.0         PSGallery            PowerShellGet
```

The command finds packages from registered package providers.

### Example 2: Find all package from a provider

```powershell
PS C:\> Find-Package -Provider PowerShellGet

Name                                     Version         Source               Provider
----                                     -------         ----------           --------
Microsoft.PowerShell.Archive             1.2.5.0         PSGallery            PowerShellGet
Microsoft.PowerShell.ConsoleGuiTools     0.7.2.0         PSGallery            PowerShellGet
```

The command finds packages from `PowerShellGet` package provider.

## PARAMETERS

### -Name

Specifies one or more package name.

```yaml
Type: String[]
Parameter Sets: Name
Aliases:

Required: False
Position: 0
Default value: *
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: True
```

### -Prerelease

Specifies if prerelease packages should be returned.

```yaml
Type: SwitchParameter
Parameter Sets: Name
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
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

### -Source

Specifies the package source.

```yaml
Type: String
Parameter Sets: Name
Aliases: Repository

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
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
Parameter Sets: Name
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -LiteralPath

Specifies a path to one or more locations.
The value of LiteralPath is used exactly as it's typed.
No characters are interpreted as wildcards.
If the path includes escape characters, enclose it in single quotation marks.
Single quotation marks tell PowerShell to not interpret any characters as escape sequences.

```yaml
Type: String[]
Parameter Sets: LiteralPath
Aliases: PSPath

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Path

Specifies a path to one or more locations.
Wildcards are accepted.

```yaml
Type: String[]
Parameter Sets: Path
Aliases: FilePath

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### -Uri

Specifies a Uri.

```yaml
Type: Uri[]
Parameter Sets: Uri
Aliases:

Required: True
Position: Named
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

[Get-Package](Get-Package.md)

[Install-Package](Install-Package.md)

[Publish-Package](Publish-Package.md)

[Save-Package](Save-Package.md)

[Update-Package](Update-Package.md)

[Uninstall-Package](Uninstall-Package.md)
