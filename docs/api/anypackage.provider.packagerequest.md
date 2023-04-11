---
parent: API
---

# PackageRequest

Namespace: AnyPackage.Provider

The `PackageRequest` class is used
 to send information to the package provider.

```csharp
public sealed class PackageRequest : Request
```

Inheritance [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object) → [Request](./anypackage.provider.request.md) → [PackageRequest](./anypackage.provider.packagerequest.md)

## Properties

### **Name**

Gets the package name.

```csharp
public string Name { get; internal set; }
```

#### Property Value

[String](https://docs.microsoft.com/en-us/dotnet/api/system.string)<br>

### **Version**

Gets the package version range.

```csharp
public PackageVersionRange Version { get; internal set; }
```

#### Property Value

[PackageVersionRange](./anypackage.provider.packageversionrange.md)<br>

### **Source**

Gets the package source name.

```csharp
public string Source { get; internal set; }
```

#### Property Value

[String](https://docs.microsoft.com/en-us/dotnet/api/system.string)<br>

### **Prerelease**

Gets if should include prerelease versions.

```csharp
public bool Prerelease { get; internal set; }
```

#### Property Value

[Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean)<br>

### **Package**

Gets the package if passed in via `InputObject` parameter.

```csharp
public PackageInfo Package { get; internal set; }
```

#### Property Value

[PackageInfo](./anypackage.provider.packageinfo.md)<br>

### **Path**

Gets the path parameter.

```csharp
public string Path { get; internal set; }
```

#### Property Value

[String](https://docs.microsoft.com/en-us/dotnet/api/system.string)<br>

### **Uri**

Gets Uri parameter.

```csharp
public Uri Uri { get; internal set; }
```

#### Property Value

Uri<br>

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

### **IsMatch(PackageVersion)**

Checks if the version satisfies the request.

```csharp
public bool IsMatch(PackageVersion version)
```

#### Parameters

`version` [PackageVersion](./anypackage.provider.packageversion.md)<br>
Specifies the version.

#### Returns

[Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean)<br>

            Returns true if the version satisfies the version range requirements.

### **IsMatch(String, PackageVersion)**

Checks if the package name and version satisfies the request.

```csharp
public bool IsMatch(string name, PackageVersion version)
```

#### Parameters

`name` [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)<br>
Specifies the name.

`version` [PackageVersion](./anypackage.provider.packageversion.md)<br>
Specifies the version.

#### Returns

[Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean)<br>

            Returns true if the name and version satisfies the request.

### **PromptUntrustedSource(String)**

Prompts the user if they want to install a package from an untrusted source.

```csharp
public bool PromptUntrustedSource(string source)
```

#### Parameters

`source` [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)<br>
Source name.

#### Returns

[Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean)<br>

            Returns true if the user accepted or false if the user rejected.

### **WritePackage(PackageInfo)**

Writes the package to the pipeline.

```csharp
public void WritePackage(PackageInfo package)
```

#### Parameters

`package` [PackageInfo](./anypackage.provider.packageinfo.md)<br>
The package.
