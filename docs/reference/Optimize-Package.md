---
external help file: AnyPackage.dll-Help.xml
Module Name: AnyPackage
online version: https://go.anypackage.dev/Optimize-Package
parent: AnyPackage
schema: 2.0.0
---

# Optimize-Package

## SYNOPSIS

Removes outdated packages.

## SYNTAX

```text
Optimize-Package [[-Name] <string[]>] [-Provider <string>] [-PassThru]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION

Removes outdated packages.

## EXAMPLES

### Example 1: Optimize all packages

```powershell
Optimize-Package

Name                                     Version         Source               Provider
----                                     -------         ----------           --------
Microsoft.PowerShell.Archive             1.2.5.0         PSGallery            PowerShellGet
Microsoft.PowerShell.ConsoleGuiTools     0.7.2.0         PSGallery            PowerShellGet
```

The command removes outdated packages from registered package providers.

### Example 2: Optimize all package from a provider

```powershell
Optimize-Package -Provider PowerShellGet

Name                                     Version         Source               Provider
----                                     -------         ----------           --------
Microsoft.PowerShell.Archive             1.2.5.0         PSGallery            PowerShellGet
Microsoft.PowerShell.ConsoleGuiTools     0.7.2.0         PSGallery            PowerShellGet
```

The command removes outdated packages from `PowerShellGet` package provider.

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

### CommonParameters

This cmdlet supports the common parameters: -Debug, -ErrorAction,
-ErrorVariable, -InformationAction, -InformationVariable, -OutVariable,
-OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.
For more information, see
[about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### System.String, AnyPackage.Provider.PackageVersionRange

You can pipe a package name to this cmdlet.

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
