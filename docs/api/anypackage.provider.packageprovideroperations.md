---
parent: API
---

# PackageProviderOperations

Namespace: AnyPackage.Provider

The supported operations for a package provider.

```csharp
public enum PackageProviderOperations
```

Inheritance [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object) → [ValueType](https://docs.microsoft.com/en-us/dotnet/api/system.valuetype) → [Enum](https://docs.microsoft.com/en-us/dotnet/api/system.enum) → [PackageProviderOperations](./anypackage.provider.packageprovideroperations.md)<br>
Implements [IComparable](https://docs.microsoft.com/en-us/dotnet/api/system.icomparable), [IFormattable](https://docs.microsoft.com/en-us/dotnet/api/system.iformattable), [IConvertible](https://docs.microsoft.com/en-us/dotnet/api/system.iconvertible)

## Fields

| Name | Value | Description |
| --- | --: | --- |
| None | 0 | The package provider does not support any operations. |
| Find | 1 | The package provider supports the Find-Package command. |
| Get | 2 | The package provider supports the Get-Package command. |
| Publish | 4 | The package provider supports the Publish-Package command. |
| Install | 8 | The package provider supports the Install-Package command. |
| Save | 16 | The package provider supports the Save-Package command. |
| Uninstall | 32 | The package provider supports the Uninstall-Package command. |
| Unpublish | 64 | The package provider supports the Unpublish-Package command. |
| Update | 128 | The package provider supports the Update-Package command. |
| GetSource | 256 | The package provider supports the Get-PackageSource command. |
| SetSource | 512 | The package provider supports the Register-PackageSource,
            Set-PackageSource, and Unregister-PackageSource command. |
