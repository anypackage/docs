# PackageDependency

Namespace: AnyPackage.Provider

The `PackageDependency` class.
 Contains information about package dependency requirements.

```csharp
public sealed class PackageDependency
```

Inheritance [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object) → [PackageDependency](./anypackage.provider.packagedependency.md)

## Properties

### **Name**

Gets the package name.

```csharp
public string Name { get; }
```

#### Property Value

[String](https://docs.microsoft.com/en-us/dotnet/api/system.string)<br>

### **VersionRange**

Gets the version range.

```csharp
public PackageVersionRange VersionRange { get; }
```

#### Property Value

[PackageVersionRange](./anypackage.provider.packageversionrange.md)<br>

### **Provider**

Gets the package provider.

```csharp
public PackageProviderInfo Provider { get; }
```

#### Property Value

[PackageProviderInfo](./anypackage.provider.packageproviderinfo.md)<br>

**Remarks:**

If null the current provider should be used.

## Constructors

### **PackageDependency(String)**

Constructs a new instance of the `PackageDependency` class.

```csharp
public PackageDependency(string name)
```

#### Parameters

`name` [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)<br>
Package name.

### **PackageDependency(String, PackageVersionRange)**

Constructs a new instance of the `PackageDependency` class.

```csharp
public PackageDependency(string name, PackageVersionRange versionRange)
```

#### Parameters

`name` [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)<br>
Package name.

`versionRange` [PackageVersionRange](./anypackage.provider.packageversionrange.md)<br>
Version range.

### **PackageDependency(String, PackageProviderInfo)**

Constructs a new instance of the `PackageDependency` class.

```csharp
public PackageDependency(string name, PackageProviderInfo provider)
```

#### Parameters

`name` [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)<br>
Package name.

`provider` [PackageProviderInfo](./anypackage.provider.packageproviderinfo.md)<br>
Package provider.

### **PackageDependency(String, PackageVersionRange, PackageProviderInfo)**

Constructs a new instance of the `PackageDependency` class.

```csharp
public PackageDependency(string name, PackageVersionRange versionRange, PackageProviderInfo provider)
```

#### Parameters

`name` [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)<br>
Package name.

`versionRange` [PackageVersionRange](./anypackage.provider.packageversionrange.md)<br>
Version range.

`provider` [PackageProviderInfo](./anypackage.provider.packageproviderinfo.md)<br>
Package provider.

## Methods

### **ToString()**

Returns a string of the package name.

```csharp
public string ToString()
```

#### Returns

[String](https://docs.microsoft.com/en-us/dotnet/api/system.string)<br>

            The package name.
