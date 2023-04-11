---
parent: API
---

# PackageInfo

Namespace: AnyPackage.Provider

The `PackageInfo` class.

```csharp
public sealed class PackageInfo
```

Inheritance [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object) → [PackageInfo](./anypackage.provider.packageinfo.md)

## Properties

### **Name**

Gets the package name.

```csharp
public string Name { get; }
```

#### Property Value

[String](https://docs.microsoft.com/en-us/dotnet/api/system.string)<br>

### **Version**

Gets the package version.

```csharp
public PackageVersion Version { get; }
```

#### Property Value

[PackageVersion](./anypackage.provider.packageversion.md)<br>

### **Description**

Gets the package description.

```csharp
public string Description { get; }
```

#### Property Value

[String](https://docs.microsoft.com/en-us/dotnet/api/system.string)<br>

### **Source**

Gets the package source.

```csharp
public PackageSourceInfo Source { get; }
```

#### Property Value

[PackageSourceInfo](./anypackage.provider.packagesourceinfo.md)<br>

### **Metadata**

Gets additional metadata about the package.

```csharp
public IReadOnlyDictionary<string, object> Metadata { get; }
```

#### Property Value

[IReadOnlyDictionary&lt;String, Object&gt;](https://docs.microsoft.com/en-us/dotnet/api/system.collections.generic.ireadonlydictionary-2)<br>

### **Provider**

Gets the package provider.

```csharp
public PackageProviderInfo Provider { get; }
```

#### Property Value

[PackageProviderInfo](./anypackage.provider.packageproviderinfo.md)<br>

### **Dependencies**

Gets package dependencies.

```csharp
public IEnumerable<PackageDependency> Dependencies { get; }
```

#### Property Value

[IEnumerable&lt;PackageDependency&gt;](https://docs.microsoft.com/en-us/dotnet/api/system.collections.generic.ienumerable-1)<br>

## Constructors

### **PackageInfo(String, PackageProviderInfo)**

Instantiates a `PackageInfo` object.

```csharp
public PackageInfo(string name, PackageProviderInfo provider)
```

#### Parameters

`name` [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)<br>
Package name.

`provider` [PackageProviderInfo](./anypackage.provider.packageproviderinfo.md)<br>
Package provider info.

### **PackageInfo(String, PackageVersion, PackageProviderInfo)**

Instantiates a `PackageInfo` object.

```csharp
public PackageInfo(string name, PackageVersion version, PackageProviderInfo provider)
```

#### Parameters

`name` [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)<br>
Package name.

`version` [PackageVersion](./anypackage.provider.packageversion.md)<br>
Package version.

`provider` [PackageProviderInfo](./anypackage.provider.packageproviderinfo.md)<br>
Package provider info.

### **PackageInfo(String, PackageVersion, String, PackageProviderInfo)**

Instantiates a `PackageInfo` object.

```csharp
public PackageInfo(string name, PackageVersion version, string description, PackageProviderInfo provider)
```

#### Parameters

`name` [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)<br>
Package name.

`version` [PackageVersion](./anypackage.provider.packageversion.md)<br>
Package version.

`description` [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)<br>
Package description.

`provider` [PackageProviderInfo](./anypackage.provider.packageproviderinfo.md)<br>
Package provider info.

### **PackageInfo(String, PackageVersion, PackageSourceInfo, PackageProviderInfo)**

Instantiates a `PackageInfo` object.

```csharp
public PackageInfo(string name, PackageVersion version, PackageSourceInfo source, PackageProviderInfo provider)
```

#### Parameters

`name` [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)<br>
Package name.

`version` [PackageVersion](./anypackage.provider.packageversion.md)<br>
Package version.

`source` [PackageSourceInfo](./anypackage.provider.packagesourceinfo.md)<br>
Package source.

`provider` [PackageProviderInfo](./anypackage.provider.packageproviderinfo.md)<br>
Package provider info.

### **PackageInfo(String, PackageVersion, PackageSourceInfo, String, PackageProviderInfo)**

Instantiates a `PackageInfo` object.

```csharp
public PackageInfo(string name, PackageVersion version, PackageSourceInfo source, string description, PackageProviderInfo provider)
```

#### Parameters

`name` [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)<br>
Package name.

`version` [PackageVersion](./anypackage.provider.packageversion.md)<br>
Package version.

`source` [PackageSourceInfo](./anypackage.provider.packagesourceinfo.md)<br>
Package source.

`description` [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)<br>
Package description.

`provider` [PackageProviderInfo](./anypackage.provider.packageproviderinfo.md)<br>
Package provider info.

### **PackageInfo(String, PackageVersion, PackageSourceInfo, String, IEnumerable&lt;PackageDependency&gt;, PackageProviderInfo)**

Instantiates a `PackageInfo` object.

```csharp
public PackageInfo(string name, PackageVersion version, PackageSourceInfo source, string description, IEnumerable<PackageDependency> dependencies, PackageProviderInfo provider)
```

#### Parameters

`name` [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)<br>
Package name.

`version` [PackageVersion](./anypackage.provider.packageversion.md)<br>
Package version.

`source` [PackageSourceInfo](./anypackage.provider.packagesourceinfo.md)<br>
Package source.

`description` [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)<br>
Package description.

`dependencies` [IEnumerable&lt;PackageDependency&gt;](https://docs.microsoft.com/en-us/dotnet/api/system.collections.generic.ienumerable-1)<br>
Package dependencies.

`provider` [PackageProviderInfo](./anypackage.provider.packageproviderinfo.md)<br>
Package provider info.

### **PackageInfo(String, PackageVersion, PackageSourceInfo, String, IEnumerable&lt;PackageDependency&gt;, IDictionary&lt;String, Object&gt;, PackageProviderInfo)**

Instantiates a `PackageInfo` object.

```csharp
public PackageInfo(string name, PackageVersion version, PackageSourceInfo source, string description, IEnumerable<PackageDependency> dependencies, IDictionary<string, object> metadata, PackageProviderInfo provider)
```

#### Parameters

`name` [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)<br>
Package name.

`version` [PackageVersion](./anypackage.provider.packageversion.md)<br>
Package version.

`source` [PackageSourceInfo](./anypackage.provider.packagesourceinfo.md)<br>
Package source.

`description` [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)<br>
Package description.

`dependencies` [IEnumerable&lt;PackageDependency&gt;](https://docs.microsoft.com/en-us/dotnet/api/system.collections.generic.ienumerable-1)<br>
Package dependencies.

`metadata` [IDictionary&lt;String, Object&gt;](https://docs.microsoft.com/en-us/dotnet/api/system.collections.generic.idictionary-2)<br>
Additional package metadata.

`provider` [PackageProviderInfo](./anypackage.provider.packageproviderinfo.md)<br>
Package provider info.

### **PackageInfo(String, PackageVersion, PackageSourceInfo, String, IEnumerable&lt;PackageDependency&gt;, Hashtable, PackageProviderInfo)**

Instantiates a `PackageInfo` object.

```csharp
public PackageInfo(string name, PackageVersion version, PackageSourceInfo source, string description, IEnumerable<PackageDependency> dependencies, Hashtable metadata, PackageProviderInfo provider)
```

#### Parameters

`name` [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)<br>
Package name.

`version` [PackageVersion](./anypackage.provider.packageversion.md)<br>
Package version.

`source` [PackageSourceInfo](./anypackage.provider.packagesourceinfo.md)<br>
Package source.

`description` [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)<br>
Package description.

`dependencies` [IEnumerable&lt;PackageDependency&gt;](https://docs.microsoft.com/en-us/dotnet/api/system.collections.generic.ienumerable-1)<br>
Package dependencies.

`metadata` [Hashtable](https://docs.microsoft.com/en-us/dotnet/api/system.collections.hashtable)<br>
Additional package metadata.

`provider` [PackageProviderInfo](./anypackage.provider.packageproviderinfo.md)<br>
Package provider info.

## Methods

### **ToString()**

Returns a string of the package name.

```csharp
public string ToString()
```

#### Returns

[String](https://docs.microsoft.com/en-us/dotnet/api/system.string)<br>

            The package name.
