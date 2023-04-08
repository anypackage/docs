---
external help file: AnyPackage.dll-Help.xml
Module Name: AnyPackage
online version: https://go.anypackage.dev/Get-PackageSource
parent: AnyPackage
schema: 2.0.0
---

# Get-PackageSource

## SYNOPSIS

Gets the package source.

## SYNTAX

```
Get-PackageSource [[-Name] <String[]>] [-Provider <String>]
 [<CommonParameters>]
```

## DESCRIPTION

Gets the package source.

## EXAMPLES

### Example 1

```powershell
PS C:\> Get-PackageSource

Name                           Location                                           Trusted
----                           --------                                           -------
PSGallery                      https://www.powershellgallery.com/api/v2           True
```

This command gets all package repositories.

## PARAMETERS

### -Name

Specifies the package source name.

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
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters

This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### System.String

You can pipe a package source to this cmdlet.

## OUTPUTS

### AnyPackage.Provider.PackageSourceInfo

This cmdlet returns objects that represent a package source.

## NOTES

## RELATED LINKS

[Register-PackageSource](Register-PackageSource.md)

[Set-PackageSource](Set-PackageSource.md)

[Unregister-PackageSource](Unregister-PackageSource.md)
