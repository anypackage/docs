---
parent: API
---

# PackageVersionRange

Namespace: AnyPackage.Provider

The `PackageVersionRange`.

```csharp
public sealed class PackageVersionRange
```

Inheritance [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object) → [PackageVersionRange](./anypackage.provider.packageversionrange.md)

## Properties

### **MinVersion**

Gets the minimum package version.

```csharp
public PackageVersion MinVersion { get; }
```

#### Property Value

[PackageVersion](./anypackage.provider.packageversion.md)<br>

### **MaxVersion**

Gets the maximum package version.

```csharp
public PackageVersion MaxVersion { get; }
```

#### Property Value

[PackageVersion](./anypackage.provider.packageversion.md)<br>

### **IsMinInclusive**

Gets if the minimum version is inclusive.

```csharp
public bool IsMinInclusive { get; }
```

#### Property Value

[Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean)<br>

### **IsMaxInclusive**

Gets if the maximum version is inclusive.

```csharp
public bool IsMaxInclusive { get; }
```

#### Property Value

[Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean)<br>

## Constructors

### **PackageVersionRange(String)**

Constructs a version range using a PowerShell modified NuGet package version range syntax.

```csharp
public PackageVersionRange(string versionRange)
```

#### Parameters

`versionRange` [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)<br>
NuGet package version formatted string.

#### Exceptions

[ArgumentNullException](https://docs.microsoft.com/en-us/dotnet/api/system.argumentnullexception)<br>
Version range is null.

[ArgumentException](https://docs.microsoft.com/en-us/dotnet/api/system.argumentexception)<br>
Version range is not in correct format.

[ArgumentOutOfRangeException](https://docs.microsoft.com/en-us/dotnet/api/system.argumentoutofrangeexception)<br>
Min version is higher than max version.

**Remarks:**

To maintain type conversion compatibility with the PowerShell cmdlet parameters
 the default behavior is to change min version syntax into required.
 For example, `1.0` would become `[1.0]` since PowerShell users expect the version
 to be the exact version supplied instead of NuGet syntax of min version inclusive.
 To pass a min version inclusive use `[1.0,]` syntax.

This behavior is only used when constructing the version range.
 The standard NuGet syntax is used elsewhere.
 If you need to use NuGet syntax use the constructor with useNuGetSyntax parameter.

### **PackageVersionRange(String, Boolean)**

Constructs a version range using a NuGet package version range syntax.

```csharp
public PackageVersionRange(string versionRange, bool useNuGetSyntax)
```

#### Parameters

`versionRange` [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)<br>
NuGet package version formatted string.

`useNuGetSyntax` [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean)<br>

            If true use NuGet syntax otherwise false uses PowerShell modified syntax.

#### Exceptions

[ArgumentNullException](https://docs.microsoft.com/en-us/dotnet/api/system.argumentnullexception)<br>
Version range is null.

[ArgumentException](https://docs.microsoft.com/en-us/dotnet/api/system.argumentexception)<br>
Version range is not in correct format.

[ArgumentOutOfRangeException](https://docs.microsoft.com/en-us/dotnet/api/system.argumentoutofrangeexception)<br>
Min version is higher than max version.

**Remarks:**

To maintain type conversion compatibility with the PowerShell cmdlet parameters
 the default behavior is to change min version syntax into required.
 For example, 1.0 would become [1.0] since PowerShell users expect the version
 to be the exact version supplied instead of NuGet syntax of min version inclusive.
 To pass a min version inclusive use `[1.0,]` syntax.

This behavior is only used when constructing the version range.
 The standard NuGet syntax is used elsewhere.
 If you need to use NuGet syntax use the useNuGetSyntax parameter.

### **PackageVersionRange(PackageVersion, PackageVersion, Boolean, Boolean)**

Constructs a version range using min and max version.

```csharp
public PackageVersionRange(PackageVersion minVersion, PackageVersion maxVersion, bool isMinInclusive, bool isMaxInclusive)
```

#### Parameters

`minVersion` [PackageVersion](./anypackage.provider.packageversion.md)<br>
Minimum version.

`maxVersion` [PackageVersion](./anypackage.provider.packageversion.md)<br>
Maximum version.

`isMinInclusive` [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean)<br>
If min version is inclusive.

`isMaxInclusive` [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean)<br>
If max version is inclusive.

#### Exceptions

[ArgumentOutOfRangeException](https://docs.microsoft.com/en-us/dotnet/api/system.argumentoutofrangeexception)<br>
Min version is higher than max version.

## Methods

### **Parse(String)**

Converts the string representation of a version range to an equivalent `PackageVersionRange` object.

```csharp
public static PackageVersionRange Parse(string versionRange)
```

#### Parameters

`versionRange` [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)<br>
A string that contains a version range to convert.

#### Returns

[PackageVersionRange](./anypackage.provider.packageversionrange.md)<br>

            An object that is equivalent to the version range specified in the versionRange parameter.

#### Exceptions

[ArgumentNullException](https://docs.microsoft.com/en-us/dotnet/api/system.argumentnullexception)<br>
Version range is null.

[ArgumentException](https://docs.microsoft.com/en-us/dotnet/api/system.argumentexception)<br>
Version range is not in correct format.

[ArgumentOutOfRangeException](https://docs.microsoft.com/en-us/dotnet/api/system.argumentoutofrangeexception)<br>
Min version is higher than max version.

**Remarks:**

To maintain type conversion compatibility with the PowerShell cmdlet parameters
 the default behavior is to change min version syntax into required.
 For example, `1.0` would become `[1.0]` since PowerShell users expect the version
 to be the exact version supplied instead of NuGet syntax of min version inclusive.
 To pass a min version inclusive use `[1.0,]` syntax.

This behavior is only used when constructing the version range.
 The standard NuGet syntax is used elsewhere.
 If you need to use NuGet syntax use the Parse method with useNuGetSyntax parameter.

### **Parse(String, Boolean)**

Converts the string representation of a version range to an equivalent `PackageVersionRange` object.

```csharp
public static PackageVersionRange Parse(string versionRange, bool useNuGetSyntax)
```

#### Parameters

`versionRange` [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)<br>
A string that contains a version range to convert.

`useNuGetSyntax` [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean)<br>

            If true use NuGet syntax otherwise false uses PowerShell modified syntax.

#### Returns

[PackageVersionRange](./anypackage.provider.packageversionrange.md)<br>

            An object that is equivalent to the version range specified in the versionRange parameter.

#### Exceptions

[ArgumentNullException](https://docs.microsoft.com/en-us/dotnet/api/system.argumentnullexception)<br>
Version range is null.

[ArgumentException](https://docs.microsoft.com/en-us/dotnet/api/system.argumentexception)<br>
Version range is not in correct format.

[ArgumentOutOfRangeException](https://docs.microsoft.com/en-us/dotnet/api/system.argumentoutofrangeexception)<br>
Min version is higher than max version.

**Remarks:**

To maintain type conversion compatibility with the PowerShell cmdlet parameters
 the default behavior is to change min version syntax into required.
 For example, `1.0` would become `[1.0]` since PowerShell users expect the version
 to be the exact version supplied instead of NuGet syntax of min version inclusive.
 To pass a min version inclusive use `[1.0,]` syntax.

This behavior is only used when constructing the version range.
 The standard NuGet syntax is used elsewhere.
 If you need to use NuGet syntax use the useNuGetSyntax parameter.

### **TryParse(String, PackageVersionRange&)**

Tries to convert the string representation of a
 version to an equivalent `PackageVersionRange` object,
 and returns a value that indicates whether the conversion succeeded.

```csharp
public static bool TryParse(string versionRange, PackageVersionRange& result)
```

#### Parameters

`versionRange` [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)<br>
A string that contains a version range to convert.

`result` [PackageVersionRange&](./anypackage.provider.packageversionrange&.md)<br>

            When this methods returns, contains the PackageVersionRange equivalent of the string, if the conversion succeeded.
            If version is null, Empty, or if the conversion fails, result is null when the method returns.

#### Returns

[Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean)<br>
true if the version parameter was converted successfully; otherwise, false.

### **TryParse(String, Boolean, PackageVersionRange&)**

Tries to convert the string representation of a
 version to an equivalent `PackageVersionRange` object,
 and returns a value that indicates whether the conversion succeeded.

```csharp
public static bool TryParse(string versionRange, bool useNuGetSyntax, PackageVersionRange& result)
```

#### Parameters

`versionRange` [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)<br>
A string that contains a version range to convert.

`useNuGetSyntax` [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean)<br>

            If true use NuGet syntax otherwise false uses PowerShell modified syntax.

`result` [PackageVersionRange&](./anypackage.provider.packageversionrange&.md)<br>

            When this methods returns, contains the PackageVersionRange equivalent of the string, if the conversion succeeded.
            If version is null, Empty, or if the conversion fails, result is null when the method returns.

#### Returns

[Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean)<br>
true if the version parameter was converted successfully; otherwise, false.

**Remarks:**

To maintain type conversion compatibility with the PowerShell cmdlet parameters
 the default behavior is to change min version syntax into required.
 For example, `1.0` would become `[1.0]` since PowerShell users expect the version
 to be the exact version supplied instead of NuGet syntax of min version inclusive.
 To pass a min version inclusive use `[1.0,]` syntax.

This behavior is only used when constructing the version range.
 The standard NuGet syntax is used elsewhere.
 If you need to use NuGet syntax use the useNuGetSyntax parameter.

### **Satisfies(PackageVersion)**

Checks the supplied version satisfies the version range.

```csharp
public bool Satisfies(PackageVersion version)
```

#### Parameters

`version` [PackageVersion](./anypackage.provider.packageversion.md)<br>
The package version to check.

#### Returns

[Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean)<br>
Returns true if the version range is satisfied by the supplied version.

### **Satisfies(PackageVersion, IComparer&lt;PackageVersion&gt;)**

Checks the supplied version satisfies the version range.

```csharp
public bool Satisfies(PackageVersion version, IComparer<PackageVersion> comparer)
```

#### Parameters

`version` [PackageVersion](./anypackage.provider.packageversion.md)<br>
The package version to check.

`comparer` [IComparer&lt;PackageVersion&gt;](https://docs.microsoft.com/en-us/dotnet/api/system.collections.generic.icomparer-1)<br>
The custom comparer to use for version comparisons.

#### Returns

[Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean)<br>
Returns true if the version range is satisfied by the supplied version.

### **ToString()**

Provides a `ToString` implementation.

```csharp
public string ToString()
```

#### Returns

[String](https://docs.microsoft.com/en-us/dotnet/api/system.string)<br>
A NuGet package version reference string.

**Remarks:**

For more information refer to: https://docs.microsoft.com/en-us/nuget/concepts/package-versioning

### **ToString(Boolean)**

Provides a `ToString` implementation.

```csharp
public string ToString(bool shortNotation)
```

#### Parameters

`shortNotation` [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean)<br>
Min version inclusive will return just the version.

#### Returns

[String](https://docs.microsoft.com/en-us/dotnet/api/system.string)<br>
A NuGet package version reference string with short notation.
