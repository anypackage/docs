---
parent: API
---

# SourceRequest

Namespace: AnyPackage.Provider

The `SourceRequest` class is used
 to send information to the package provider.

```csharp
public sealed class SourceRequest : Request
```

Inheritance [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object) → [Request](./anypackage.provider.request.md) → [SourceRequest](./anypackage.provider.sourcerequest.md)

## Properties

### **Name**

Gets the package source name.

```csharp
public string Name { get; internal set; }
```

#### Property Value

[String](https://docs.microsoft.com/en-us/dotnet/api/system.string)<br>

### **Location**

Gets the package source location.

```csharp
public string Location { get; internal set; }
```

#### Property Value

[String](https://docs.microsoft.com/en-us/dotnet/api/system.string)<br>

### **Trusted**

Gets if the package source is trusted.

```csharp
public Nullable<bool> Trusted { get; internal set; }
```

#### Property Value

[Nullable&lt;Boolean&gt;](https://docs.microsoft.com/en-us/dotnet/api/system.nullable-1)<br>

### **Force**

Gets if the source should be overwritten.

```csharp
public Nullable<bool> Force { get; internal set; }
```

#### Property Value

[Nullable&lt;Boolean&gt;](https://docs.microsoft.com/en-us/dotnet/api/system.nullable-1)<br>

### **Source**

Gets the package source if passed in via `InputObject` parameter.

```csharp
public PackageSourceInfo Source { get; internal set; }
```

#### Property Value

[PackageSourceInfo](./anypackage.provider.packagesourceinfo.md)<br>

### **DynamicParameters**

Gets the package provider dynamic parameters.

```csharp
public object DynamicParameters { get; internal set; }
```

#### Property Value

[Object](https://docs.microsoft.com/en-us/dotnet/api/system.object)<br>

### **ParameterSetName**

Gets the parameter set name.

```csharp
public string ParameterSetName { get; }
```

#### Property Value

[String](https://docs.microsoft.com/en-us/dotnet/api/system.string)<br>

### **Stopping**

Gets if the package provider has been requested to stop.

```csharp
public bool Stopping { get; }
```

#### Property Value

[Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean)<br>

### **ProviderInfo**

Gets the package provider information.

```csharp
public PackageProviderInfo ProviderInfo { get; internal set; }
```

#### Property Value

[PackageProviderInfo](./anypackage.provider.packageproviderinfo.md)<br>

## Methods

### **IsMatch(String)**

Checks if the name satisfies the request.

```csharp
public bool IsMatch(string name)
```

#### Parameters

`name` [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)<br>
Specifies the name.

#### Returns

[Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean)<br>

            Returns true if the name is a wildcard match to the request.

**Remarks:**

Case is ignored during comparison.

### **WriteSource(PackageSourceInfo)**

Writes the package source to the pipeline.

```csharp
public void WriteSource(PackageSourceInfo source)
```

#### Parameters

`source` [PackageSourceInfo](./anypackage.provider.packagesourceinfo.md)<br>
The package source.
