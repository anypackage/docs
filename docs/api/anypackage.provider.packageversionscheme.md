# PackageVersionScheme

Namespace: AnyPackage.Provider

Supported package version schemes.

```csharp
public enum PackageVersionScheme
```

Inheritance [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object) → [ValueType](https://docs.microsoft.com/en-us/dotnet/api/system.valuetype) → [Enum](https://docs.microsoft.com/en-us/dotnet/api/system.enum) → [PackageVersionScheme](./anypackage.provider.packageversionscheme.md)<br>
Implements [IComparable](https://docs.microsoft.com/en-us/dotnet/api/system.icomparable), [IFormattable](https://docs.microsoft.com/en-us/dotnet/api/system.iformattable), [IConvertible](https://docs.microsoft.com/en-us/dotnet/api/system.iconvertible)

## Fields

| Name | Value | Description |
| --- | --: | --- |
| AlphaNumeric | 0 | Alpha-numeric version. |
| Integer | 1 | Single integer value. |
| MultiPartNumeric | 2 | Multiple part numeric. |
| MultiPartNumericSuffix | 3 | Multiple part numeric with alpha-numeric suffix. |
| SemanticVersion | 4 | Version adheres to the semver 2.0 spec. |
