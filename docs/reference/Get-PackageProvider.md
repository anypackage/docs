---
external help file: AnyPackage.dll-Help.xml
Module Name: AnyPackage
online version: https://go.anypackage.dev/Get-PackageProvider
parent: AnyPackage
schema: 2.0.0
---

# Get-PackageProvider

## SYNOPSIS

Gets imported package providers.

## SYNTAX

```none
Get-PackageProvider [[-Name] <String[]>] [-ListAvailable]
 [<CommonParameters>]
```

## DESCRIPTION

Gets imported package providers.

## EXAMPLES

### Example 1

```powershell
PS C:\> Get-PackageProvider

Name                 Priority Operations
----                 -------- ----------
msu                       100 Get
PowerShellGet             100 Find, Get, Publish, Install, Save, Uninstall, Update, GetSource, SetSource
```

The command gets the imported package providers.

## PARAMETERS

### -Name

Specifies the package provider name.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: Provider

Required: False
Position: 0
Default value: *
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: True
```

### -ListAvailable

Get list of available package providers in modules in `$env:PSModulePath`.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters

This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### System.String

You can pipe a package provider name to this cmdlet.

## OUTPUTS

### AnyPackage.Provider.PackageProviderInfo

This cmdlet returns objects that represent a package provider.

## NOTES

## RELATED LINKS

[Import-Module](https://learn.microsoft.com/en-us/powershell/module/microsoft.powershell.core/import-module)

[Remove-Module](https://learn.microsoft.com/en-us/powershell/module/microsoft.powershell.core/remove-module)
