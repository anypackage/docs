# PackageProviderInfo

Namespace: AnyPackage.Provider

This class contains information about a package provider.

```csharp
public class PackageProviderInfo
```

Inheritance [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object) → [PackageProviderInfo](./anypackage.provider.packageproviderinfo.md)

## Properties

### **Name**

Gets the name of a provider.

```csharp
public string Name { get; }
```

#### Property Value

[String](https://docs.microsoft.com/en-us/dotnet/api/system.string)<br>

### **ImplementingType**

Gets the provider type.

```csharp
public Type ImplementingType { get; }
```

#### Property Value

[Type](https://docs.microsoft.com/en-us/dotnet/api/system.type)<br>

### **Id**

Gets the provider identifier.

```csharp
public Guid Id { get; }
```

#### Property Value

[Guid](https://docs.microsoft.com/en-us/dotnet/api/system.guid)<br>

### **Module**

Gets the package provider PowerShell module information.

```csharp
public PSModuleInfo Module { get; }
```

#### Property Value

PSModuleInfo<br>

### **ModuleName**

Gets the package provider PowerShell module.

```csharp
public string ModuleName { get; }
```

#### Property Value

[String](https://docs.microsoft.com/en-us/dotnet/api/system.string)<br>

### **FullName**

Gets the provider full name.

```csharp
public string FullName { get; }
```

#### Property Value

[String](https://docs.microsoft.com/en-us/dotnet/api/system.string)<br>

**Remarks:**

The provider full name is the module name and provider name.
 For example, AnyPackage\NuGet
 If the module name is null returns the provider name.

### **Version**

Gets the package provider version using the module's version.

```csharp
public Version Version { get; }
```

#### Property Value

[Version](https://docs.microsoft.com/en-us/dotnet/api/system.version)<br>

### **Operations**

Gets the package operations the provider supports.

```csharp
public PackageProviderOperations Operations { get; }
```

#### Property Value

[PackageProviderOperations](./anypackage.provider.packageprovideroperations.md)<br>

### **Priority**

Gets and sets the package provider priority.

```csharp
public byte Priority { get; set; }
```

#### Property Value

[Byte](https://docs.microsoft.com/en-us/dotnet/api/system.byte)<br>

**Remarks:**

Lower the number the higher the priority.

### **PackageByName**

Gets if the package provider supports package by name parameter set.

```csharp
public bool PackageByName { get; }
```

#### Property Value

[Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean)<br>

**Remarks:**

If `false` package provider doesn't support
 `Name` parameter set for the following cmdlets:
 Find-Package, Install-Package, Update-Package

### **PackageByFile**

Gets if the package provider supports package by path parameter set.

```csharp
public bool PackageByFile { get; }
```

#### Property Value

[Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean)<br>

### **PackageByUri**

Gets if the package provider support package by uri parameter set.

```csharp
public bool PackageByUri { get; }
```

#### Property Value

[Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean)<br>

### **FileExtensions**

Gets supported file extensions.

```csharp
public IEnumerable<string> FileExtensions { get; }
```

#### Property Value

[IEnumerable&lt;String&gt;](https://docs.microsoft.com/en-us/dotnet/api/system.collections.generic.ienumerable-1)<br>

### **UriSchemes**

Gets supported Uri schemes.

```csharp
public IEnumerable<string> UriSchemes { get; }
```

#### Property Value

[IEnumerable&lt;String&gt;](https://docs.microsoft.com/en-us/dotnet/api/system.collections.generic.ienumerable-1)<br>

## Methods

### **ToString()**

Returns provider name.

```csharp
public string ToString()
```

#### Returns

[String](https://docs.microsoft.com/en-us/dotnet/api/system.string)<br>

### **CreateInstance()**

```csharp
internal PackageProvider CreateInstance()
```

#### Returns

[PackageProvider](./anypackage.provider.packageprovider.md)<br>

### **HasOperation(PackageProviderOperations)**

```csharp
internal bool HasOperation(PackageProviderOperations operations)
```

#### Parameters

`operations` [PackageProviderOperations](./anypackage.provider.packageprovideroperations.md)<br>

#### Returns

[Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean)<br>

### **IsMatch(String)**

```csharp
internal bool IsMatch(string name)
```

#### Parameters

`name` [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)<br>

#### Returns

[Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean)<br>
