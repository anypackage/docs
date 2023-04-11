# PackageVersion

Namespace: AnyPackage.Provider

The `PackageVersion` class.

```csharp
public sealed class PackageVersion : System.IComparable, System.IComparable`1[[AnyPackage.Provider.PackageVersion, AnyPackage, Version=0.5.1.0, Culture=neutral, PublicKeyToken=null]], System.IEquatable`1[[AnyPackage.Provider.PackageVersion, AnyPackage, Version=0.5.1.0, Culture=neutral, PublicKeyToken=null]]
```

Inheritance [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object) → [PackageVersion](./anypackage.provider.packageversion.md)<br>
Implements [IComparable](https://docs.microsoft.com/en-us/dotnet/api/system.icomparable), [IComparable&lt;PackageVersion&gt;](https://docs.microsoft.com/en-us/dotnet/api/system.icomparable-1), [IEquatable&lt;PackageVersion&gt;](https://docs.microsoft.com/en-us/dotnet/api/system.iequatable-1)

## Properties

### **Version**

Gets the version.

```csharp
public string Version { get; }
```

#### Property Value

[String](https://docs.microsoft.com/en-us/dotnet/api/system.string)<br>

### **Major**

Gets the dot separated first position.

```csharp
public Nullable<ulong> Major { get; }
```

#### Property Value

[Nullable&lt;UInt64&gt;](https://docs.microsoft.com/en-us/dotnet/api/system.nullable-1)<br>

### **Minor**

Gets the dot separated second position.

```csharp
public Nullable<ulong> Minor { get; }
```

#### Property Value

[Nullable&lt;UInt64&gt;](https://docs.microsoft.com/en-us/dotnet/api/system.nullable-1)<br>

### **Patch**

Gets the dot separated third position.

```csharp
public Nullable<ulong> Patch { get; }
```

#### Property Value

[Nullable&lt;UInt64&gt;](https://docs.microsoft.com/en-us/dotnet/api/system.nullable-1)<br>

### **Revision**

Gets the dot separated fourth position.

```csharp
public Nullable<ulong> Revision { get; }
```

#### Property Value

[Nullable&lt;UInt64&gt;](https://docs.microsoft.com/en-us/dotnet/api/system.nullable-1)<br>

### **Parts**

Gets all the dot separated values.

```csharp
public IEnumerable<ulong> Parts { get; }
```

#### Property Value

[IEnumerable&lt;UInt64&gt;](https://docs.microsoft.com/en-us/dotnet/api/system.collections.generic.ienumerable-1)<br>

### **IsPrerelease**

Gets if the version is a prerelease.

```csharp
public bool IsPrerelease { get; }
```

#### Property Value

[Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean)<br>

### **Suffix**

Gets the suffix of a multi-part numeric with suffix version.

```csharp
public string Suffix { get; }
```

#### Property Value

[String](https://docs.microsoft.com/en-us/dotnet/api/system.string)<br>

### **HasMetadata**

Gets if there

```csharp
public bool HasMetadata { get; }
```

#### Property Value

[Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean)<br>

### **Prerelease**

Gets the dot separated values of the prerelease string.

```csharp
public IEnumerable<string> Prerelease { get; }
```

#### Property Value

[IEnumerable&lt;String&gt;](https://docs.microsoft.com/en-us/dotnet/api/system.collections.generic.ienumerable-1)<br>

### **Metadata**

Gets the dot separated values of the build metadata string.

```csharp
public IEnumerable<string> Metadata { get; }
```

#### Property Value

[IEnumerable&lt;String&gt;](https://docs.microsoft.com/en-us/dotnet/api/system.collections.generic.ienumerable-1)<br>

### **Scheme**

Gets the version scheme.

```csharp
public PackageVersionScheme Scheme { get; }
```

#### Property Value

[PackageVersionScheme](./anypackage.provider.packageversionscheme.md)<br>

## Constructors

### **PackageVersion(String)**

Constructs an instance of the `PackageVersion` class.

```csharp
public PackageVersion(string version)
```

#### Parameters

`version` [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)<br>
The version.

### **PackageVersion(Version)**

Constructs an instance of the `PackageVersion` class.

```csharp
public PackageVersion(Version version)
```

#### Parameters

`version` [Version](https://docs.microsoft.com/en-us/dotnet/api/system.version)<br>
The version.

## Methods

### **Parse(String)**

Converts the string representation of a version to an equivalent `PackageVersion` object.

```csharp
public static PackageVersion Parse(string version)
```

#### Parameters

`version` [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)<br>
A string that contains a version to convert.

#### Returns

[PackageVersion](./anypackage.provider.packageversion.md)<br>

            An object that is equivalent to the version specified in the version parameter.

### **TryParse(String, PackageVersion&)**

Tries to convert the string representation of a version to an equivalent `PackageVersion` object,
 and returns a value that indicates whether the conversion succeeded.

```csharp
public static bool TryParse(string version, PackageVersion& result)
```

#### Parameters

`version` [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)<br>
A string that contains a version to convert.

`result` [PackageVersion&](./anypackage.provider.packageversion&.md)<br>

            When this methods returns, contains the PackageVersion equivalent of the string, if the conversion succeeded.
            If version is null, Empty, or if the conversion fails, result is null when the method returns.

#### Returns

[Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean)<br>
true if the version parameter was converted successfully; otherwise, false.

### **ToVersion()**

A Version representation of `PackageVersion`.

```csharp
public Version ToVersion()
```

#### Returns

[Version](https://docs.microsoft.com/en-us/dotnet/api/system.version)<br>
A Version representation of PackageVersion.

### **CompareTo(Object)**

Compares this object to the other for version comparison.

```csharp
public int CompareTo(object obj)
```

#### Parameters

`obj` [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object)<br>
The version to compare against

#### Returns

[Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)<br>

            Returns -1 when this object is a lower version than the other.
            Returns 0 when this object and other object are equal.
            Returns 1 for this object is a higher version than the other.

**Remarks:**

Refer to `CompareTo(PackageVersion other)` for
 version comparison rules.

### **CompareTo(PackageVersion)**

Compares this object to the other for version comparison.

```csharp
public int CompareTo(PackageVersion other)
```

#### Parameters

`other` [PackageVersion](./anypackage.provider.packageversion.md)<br>
The version to compare against.

#### Returns

[Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)<br>

            Returns -1 when this object is a lower version than the other.
            Returns 0 when this object and other object are equal.
            Returns 1 for this object is a higher version than the other.

**Remarks:**

The sorting is by first comparing if both versions are using
 the alpha-numeric version scheme. If so then it compares using
 string comparison. If one of the two versions is alpha-numeric
 it be considered higher compared to the numeric version.

Numeric sorting takes place after it is determined neither is
 alpha-numeric. It will compare each version part numerically until
 one part is different. The version sorting is able to compare different
 version lengths (1.0 vs 1.0.0 or 1.0.0.1). If no difference is found
 it will then compare suffix and prerelease.

Versions with a suffix are considered higher than their non-suffix
 counterparts (1.0 is lower than 1.0a). If both versions contain
 a suffix they will compared using the string comparison.

Versions with a prerelease are considered lower than their non-prerelease
 counterparts (1.0 is higher than 1.0-alpha). If both versions contain a
 prerelease they will compared using the rules defined in semver 2.0.

### **Equals(PackageVersion)**

Provides an Equals implementation.

```csharp
public bool Equals(PackageVersion other)
```

#### Parameters

`other` [PackageVersion](./anypackage.provider.packageversion.md)<br>
Input object.

#### Returns

[Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean)<br>
Returns true if the objects are equal.

### **Equals(Object)**

Provides an Equals implementation.

```csharp
public bool Equals(object obj)
```

#### Parameters

`obj` [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object)<br>
Input object.

#### Returns

[Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean)<br>
Returns true if the objects are equal.

### **GetHashCode()**

Provides a GetHashCode implementation.

```csharp
public int GetHashCode()
```

#### Returns

[Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)<br>
Returns the hash code for Version property.

### **ToString()**

Provides a ToString implementation.

```csharp
public string ToString()
```

#### Returns

[String](https://docs.microsoft.com/en-us/dotnet/api/system.string)<br>
Returns the Version property.
