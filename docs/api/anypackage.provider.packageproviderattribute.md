---
parent: API
---

# PackageProviderAttribute

Namespace: AnyPackage.Provider

Identifies a class as a package provider.

```csharp
public sealed class PackageProviderAttribute : System.Attribute
```

Inheritance [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object) → [Attribute](https://docs.microsoft.com/en-us/dotnet/api/system.attribute) → [PackageProviderAttribute](./anypackage.provider.packageproviderattribute.md)

## Properties

### **Name**

Gets the provider name.

```csharp
public string Name { get; }
```

#### Property Value

[String](https://docs.microsoft.com/en-us/dotnet/api/system.string)<br>

### **FileExtensions**

Gets or sets the supported file extensions.

```csharp
public String[] FileExtensions { get; set; }
```

#### Property Value

[String[]](https://docs.microsoft.com/en-us/dotnet/api/system.string)<br>

### **UriSchemes**

Gets or sets the supported Uri schemes.

```csharp
public String[] UriSchemes { get; set; }
```

#### Property Value

[String[]](https://docs.microsoft.com/en-us/dotnet/api/system.string)<br>

### **PackageByName**

Gets if the provider supports the `Name` parameter set.

```csharp
public bool PackageByName { get; set; }
```

#### Property Value

[Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean)<br>

**Remarks:**

Used for providers that use `Path` parameter set.
 Used for the following cmdlets:
 Find-Package, Install-Package, Update-Package

### **TypeId**

```csharp
public object TypeId { get; }
```

#### Property Value

[Object](https://docs.microsoft.com/en-us/dotnet/api/system.object)<br>

## Constructors

### **PackageProviderAttribute(String)**

Constructor for the package provider attribute.

```csharp
public PackageProviderAttribute(string name)
```

#### Parameters

`name` [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)<br>
The provider name.
